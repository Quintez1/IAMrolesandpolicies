<p align="center">
<img src="https://i.imgur.com/4hzgUaF.jpeg" alt="AWS logo"/>
</p>

<h1>Lab - Create an AWS environment and configure IAM roles and policies.
 </h1>

- Simple Steps and Description:
  
We'll learn about Virtual Private Networks (VPNs) by setting up a free VPN and seeing how it changes our online location.

Steps:

- Create a Cloud Computer: Make a Windows 10 computer in the cloud.
- Sign Up for ProtonVPN: Get a free VPN account.
- Test the VPN Connection: Connect to the VPN and see how it changes our IP address.
- Browse Websites: See how websites look different when we connect from different countries.
  
This lab involves setting up and testing a Virtual Private Network (VPN) using ProtonVPN. You will create an Azure virtual machine in a different geographic location, test VPN connections, and observe how VPN affects your IP address and access to websites. This exercise helps you understand the practical use of VPNs in enhancing privacy and security.

Environments and Technologies Used:
- Azure Portal
- Windows 10 VM
- ProtonVPN
- Web Browsers
  
- Part 1: Create Virtual Machine in Azure
Record Initial IP Address:

On your local computer, go to https://whatismyipaddress.com/ and note your IP address in a text file.
Create a Resource Group and VM:

Navigate to the Azure Portal.
Create a new Resource Group.
Create a Windows 10 VM in a different geographic location (e.g., another country).
Record VM IP Address:

Log into the VM using Remote Desktop.
Go to https://whatismyipaddress.com/ and note the VM's IP address in a text file.

- Part 2: Sign up for ProtonVPN and Test VPN Connection
Sign up for ProtonVPN:

On your local computer, sign up for a free ProtonVPN account at https://account.protonvpn.com/signup?plan=free&language=en.
Set up VPN in VM:

Within the VM, download and install the ProtonVPN client.
Log in to ProtonVPN and connect to a VPN server in another country (e.g., Japan).
Go to https://whatismyipaddress.com/ and note the new IP address.
Browse Different Websites:

Try browsing to Google, Disney, and Amazon to see if there are any differences in content or language based on the VPN server location.

- Part 3: Clean up Azure Resources
Delete Resource Group:
Navigate to the Azure Portal.
Delete the Resource Group created for this lab to ensure all resources are removed.

<img src="https://i.imgur.com/aAW5sbG.png" alt="Virtual Private Network"/>
