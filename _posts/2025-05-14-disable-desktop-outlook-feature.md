---
title: "Disable This Desktop Outlook Feature"
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


## Welcome to My Blog!

This is the main content of my first blog post. I'm excited to be using the **Minimal Mistakes** theme.

It's pretty easy to get started with [Markdown](https://www.markdownguide.org/).

### Subheadings are Useful

You can structure your content with different heading levels.

* Here's a list item.
* And another one.

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
