# SMB Setup on TrueNAS  

## Overview  
SMB (Server Message Block) is a protocol used for file sharing over a network. As I have other machines connected to the server outside my home-network, I wanted a way to share files between seperate machines using applications like Windows' **File Explorer**.

## My Experience & Learning Process  
Before this project, I didn’t know much about SMB, and I assumed it was just a Windows feature. Here’s what I learned:  

- **SMB works across different operating systems**, not just Windows.  
- **User permissions and network settings are crucial**—I had issues where my devices couldn’t see the shares because I hadn’t properly configured authentication.  
- **Tailscale doesn’t automatically expose SMB shares**—I needed to modify firewall rules to allow traffic on port 445.  

## Enabling SMB  
1. Navigate to **Sharing > SMB** in TrueNAS.  
2. Click **Add** and select the dataset to share.  
3. Configure access control settings.  

## Troubleshooting  
- **Issue:** Windows devices couldn’t access the share.  
  - Solution: Enabled NTLM authentication.  
- **Issue:** Permissions weren’t working as expected.  
  - Solution: Adjusted ACL settings.
