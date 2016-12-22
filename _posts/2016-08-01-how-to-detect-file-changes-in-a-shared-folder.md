---
layout: post 
published: true 
title: "How to Detect File Changes in a Shared Folder" 
date: 2016-08-01T06:57:43.750Z
categories: security activedirectory
link: https://www.netwrix.com/detecting_file_changes_in_shared_folder.html
tags:
  - links
ogtype: article 
bodyclass: post 
---

## How to Detect File Changes in a Shared Folder
Native Auditing 

NATIVE AUDITING
Navigate to the file share, right-click it and select "Properties" → "Security" tab → "Advanced" button → "Auditing" tab → Click "Add" button Select Principal: "Everyone"; Select Type: "All"; Select Applies to: "This folder, subfolders and files"; Select the following "Advanced Permissions": сreate files/write data, сreate folders/append data, write attributes, write extended attributes.
Run gpedit.msc, configure Default Domain Policy → Computer Configuration → Policies → Windows Settings → Security Settings → Local Policies → Audit Policy → Audit object access → Define "Success and Failures". In the "Advanced Audit Policy Configuration" adjust Audit File System → Define "Success and Failures" and Audit Handle Manipulation → Define "Success and Failures".
Go to Event Log and set "Maximum security log size" to 1gb, "Retention method for Security log" to "Overwrite events as needed".
Open "Event viewer" and search Security log for event id 4656 with "File System" or "Removable Storage" task category and with "Accesses: WriteData" string. "Subject Security ID" will show you who changed the file.
