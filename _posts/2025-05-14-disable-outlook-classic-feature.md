---
title: "Disable This Outlook (Classic) Feature"
#layout: single # Uses the 'single' layout defined by Minimal Mistakes for posts
date: 2025-05-14 20:10:00 +0100 # Date and time of publication, including your timezone offset
# last_modified_at: 2025-05-14 # Optional: if you want to show when it was last updated
categories: # Optional: Helps organize your posts
  - Outlook
  - M365
  - PowerShell
  
tags: # Optional: For finer-grained filtering and SEO
  - Email
  - Outlook
  - M365
  - PowerShell
  - Meetings
#excerpt: "A short summary of your post that might appear on archive pages or in SEO results." # Optional
#header: # Optional: For adding a header image to your post
 # image: /assets/images/your-post-header-image.jpg # Path to an image in your assets folder
  #teaser: /assets/images/your-post-teaser-image.jpg # Optional: A smaller version for list pages
  #caption: "Photo credit: [Your Name](link_to_source_if_any)" # Optional
# toc: true # Optional: Set to true to automatically generate a Table of Contents
# toc_sticky: true # Optional: If toc is true, makes the TOC stick to the side as you scroll
---

If you still have users within your organisation who are yet to migrate to 'New' Outlook, you may want to consider disabling this Outlook (Classic) option.

Outlook (Classic) (by default) allows users to 'Accept' meeting/event invites without sending a response. In a time where work-from-home (WFH) is more prevalent, this is a feature that can lead to some unnecessary confusion/uncertainty for planning commissons when preparing for in-real-life (IRL) events.

Your organisations HR department or Sports & Social club may thank you for aiding them in gathering more realistic numbers when planning for the next Work Social or Christmas party!

## Outlook (Classic) Before & After

{% include figure image_path="/assets/images/Outlook-Before.png" alt="Classic Outlook before the Registry change" caption="Outlook (Classic) Before" class="align-center" %}
{% include figure image_path="/assets/images/Outlook-After.png" alt="Classic Outlook after the Registry change" caption="Outlook (Classic) After" class="align-center" %}

In order to disable the default reply options in users Outlook desktop client, its neccessary to create a registry change on the relevant users windows devices.

### Short Powershell Script to add the registry value. Run locally or deploy via Intune to targeted Windows devices.
```powershell
    # PowerShell Script
    # This script creates a new registry entry to disable the 'Do Not Send a Response' option in Outlook when attendees accept a meeting request

    # Define the registry path where you want to create the new registry key
    $registryPath = "HKCU:\Software\Microsoft\Office\16.0\Outlook\Options\Calendar"

    # Define the registry entry name and value
    $entryName = "ForceMtgResponse"
    $entryValue = 1 # DWORD value (example value)

    # Check if the registry path exists, if not, create it
    if (-not (Test-Path $registryPath)) {
    New-Item -Path $registryPath -Force
    }

    # Set the registry value
    New-ItemProperty -Path $registryPath -Name $entryName -Value $entryValue -PropertyType DWORD -Force
```
### Deploy Script via Intune

* Login to Microsoft Intune Admin Centre
* Ensure that your user account you're using has the required privilaged role assigned. E.g. Intune Administrator 
* Navigate to the Devices plane & select Windows as your platform
* Under Manage Devices -> Scripts and remediation, select 'Create' 
* Name your new custom script and leave a detailed decription of the expected behavior 
* Next, attach your script as a .ps1 file. Opt to run this script using the logged-on user credentials & run in 64-bit Powershell
* Following this, assign the script to a security group containing the users or devices you wish to target
* Schedule the frequency at which you want the script to be ran. E.g. Once per day @ 9pm
* Review and save 
* In the overview section of your script, after some time has passed, you'll receive updated information regarding your scripts perfomance on the targeted endpoints

---