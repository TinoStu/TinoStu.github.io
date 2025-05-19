---
title: "Restricting Removable Storage with Intune & Endpoint Security"
#layout: single # Uses the 'single' layout defined by Minimal Mistakes for posts
date: 2025-05-18 20:10:00 +0100 # Date and time of publication, including your timezone offset
# last_modified_at: 2025-05-14 # Optional: if you want to show when it was last updated
categories: # Optional: Helps organize your posts
  - Intune
  - Security
  
tags: # Optional: For finer-grained filtering and SEO
  - Intune
  - Security
  - M365
  - DLP
#excerpt: "A short summary of your post that might appear on archive pages or in SEO results." # Optional
#header: # Optional: For adding a header image to your post
 # image: /assets/images/your-post-header-image.jpg # Path to an image in your assets folder
  #teaser: /assets/images/your-post-teaser-image.jpg # Optional: A smaller version for list pages
  #caption: "Photo credit: [Your Name](link_to_source_if_any)" # Optional
# toc: true # Optional: Set to true to automatically generate a Table of Contents
# toc_sticky: true # Optional: If toc is true, makes the TOC stick to the side as you scroll
---

USB flash drives and other removable storage devices while convenient due to their portability and ease of use, pose a significant level of risk to an organisation's data security. 

## Unrestricted access to these devices expose an organisation to the following potential risks:

* Data Theft 
* Malware Infections
* Accidental Data Loss
* Insider Threats

---

In this post, I'll detail how you can use Microsoft Intune, along with its Endpoint Security Attack Surface Reduction capabilities to help mitigate these risks.


## Microsoft Intune & Endpoint Security Attack Surface Reduction

{% include figure image_path="/assets/images/Endpoint-Security.png" alt="Endpoint Security" caption="Endpoint Security/Attack Surface Reduction" class="align-center" %}

* Open Intune admin centre and navigate to the Endpoint security blade -> Attack surface reduction
* Within Policies, select to 'Create Policy'
* Under Platform, select 'Windows' & under Profile, select 'Device Control' & then 'Create'
* Name and give a description to your new policy

{% include figure image_path="/assets/images/Device-Control-Settings.png" alt="Device Control Settings" caption="Device Control Configuration Settings" class="align-center" %}

* Under 'Configuration Settings' select 'Storage' 
* There will be an option for 'Removable Disk Deny Write Access'; Set this option to 'Enabled'
* Additionally under 'Removable Storage Access' you'll see options to Deny Read & Write access to Windows Portable Devices. Enable these options also if required
* WDP devices include 'media players, storage devices, mobile phones and cameras'
* Next assign the policy to the intended users. 'All Users' as a target is appropriate here
* Create an exclusion group if necessary 
* Review and save the policy
* The new policy will now begin rolling out to endpoints
* Return to the policy overview page to gain insights into it's deployment & success rate
* Users will now have restricted access to removable storage 




---