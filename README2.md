# Azure Active Directory Setup Tutorial

## Overview
This tutorial provides a comprehensive guide on setting up Active Directory in Microsoft Azure. It covers setting up a Windows server to host Active Directory, configuring a client machine to connect through a shared domain, and various other essential configurations and best practices.

## Contents

### 1. Introduction to Azure Active Directory Setup
We start by introducing the installation of Active Directory through Microsoft Azure. The aim is to set up one machine as the Windows server for hosting Active Directory and another to connect to it through a shared domain.
![ADSETUPINTRO](images/ADSETUPINTRO.PNG)

### 2. Creating a Resource Group and Domain Controller
We'll create a Resource Group in Azure for managing the virtual machines. The first virtual machine, GG DC1, is set up as the domain controller using Windows Server 2019, emphasizing the same region and zone for both machines.
![RGANDDCCREATE](images/RGANDDCCREATE.PNG)

### 3. Configuring the Virtual Network and Machine Setup
Demonstrating the configuration of the VNet shared by both virtual machines. We then create the second virtual machine, J Client One, using Windows 10 Pro, ensuring it shares the same VNet as the domain controller.
![VNETCONFIG](images/VNETCONFIG.PNG)

### 4. Static IP Configuration and Remote Desktop Connection
Changing the IP configuration of the domain controller to a static IP for consistency. We then show the process for connecting to the domain controller via remote desktop.
![STATICIPANDRDC](images/STATICIPANDRDC.PNG)

### 5. Verifying the Virtual Machine Deployment
After logging into the domain controller, we check the Azure portal to confirm the successful deployment of the second virtual machine and ensure that the location and VNet settings are correctly aligned.
![VMDEPLOYCHECK](images/VMDEPLOYCHECK.PNG)

### 6. Establishing Communication and Firewall Configuration
Showing how to establish communication between the two machines using the ping command and how to navigate the Windows Firewall settings on the domain controller to enable specific rules for successful communication.
![COMMSANDFIREWALL](images/COMMSANDFIREWALL.PNG)

### 7. Active Directory Installation and Configuration
Focusing on installing and configuring Active Directory Domain Services on the domain controller. We walk through the process of adding roles and features and setting up a new forest with the domain 'jagilmor.com'.
![ADINSTALLCONFIG](images/ADINSTALLCONFIG.PNG)

### 8. User Management and Remote Desktop Access
Guiding through creating new users in Active Directory, such as 'Gilmore Zilla' and 'Jaro Saurus', and configuring remote desktop access for them. This includes adding these users to the domain and assigning them appropriate permissions.
![USERMGMTRDC](images/USERMGMTRDC.PNG)

### 9. DNS Server Configuration and Client Setup
Explaining the importance of configuring the DNS server settings on Client One to match the domain controller for seamless integration. This involves restarting Client One to update the DNS server settings.
![DNSCONFIGRESTART](images/DNSCONFIGRESTART.PNG)

### 10. Final Steps and Lockout Policy Implementation
Covering the implementation of a lockout policy in Group Policy Management to enhance security. This includes setting a threshold for failed login attempts and how to unlock a user account if it gets locked.
![LPIMPLEMENT](images/LPIMPLEMENT.PNG)

## Conclusion
This tutorial aims to provide a thorough understanding of setting up and managing Active Directory in an Azure environment. For additional resources and scripts used in this tutorial, please refer to the accompanying GitHub repository.
