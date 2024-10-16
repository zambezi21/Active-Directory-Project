# ACTIVE DIRECTORY PROJECT

## Objective

The Active Directory project aimed to establish a controlled environment for managing and securing an organization's network infrastructure. The primary focus was to configure and monitor AD services, including authentication, access control, and policy enforcement, while integrating with security tools for monitoring suspicious activities. This hands-on experience was designed to deepen understanding of identity management, security best practices, and system administration.

### Skills Learned


- User and Group Management
- Group Policy Configuration
- Authentication and Access Control
- Domain Services Setup
- Active Directory Security
- Ability to generate and recongnize attack signatures and patterns.
- Troubleshooting and Monitoring

### Tools Used

- Security Information and Event Management (SIEM) system for log ingestion and analysis(Splunk).
- Windows Server and Windows 10.
- Kali Linux.
- Event Logging tools(SYSMON).

## Steps
- The first step that was taken was to create a diagram of the project.

![Screenshot (7)](https://github.com/user-attachments/assets/3f32fe29-976e-4182-afb9-6f131d873e58)
 *Ref 1: Network Diagram*

- The second step was to install the 4 main machines that would be used for the project. This would be a Windows 10 Machine, Windows Server 2022, Splunk server, and Kali on Virual Box.
- The third step was to install and configure software that will be used(SYSMON and Splunk). This involved setting up a static ip on the Splunk server for it to use, install Splunk on the server, and running a command to make Splunk start up every time the Splunk Server VM reboots. As well as installing Sysmon and Splunk on both Windows machines as well as Splunk Universal Forwarder. Then the same steps have to be taken on the Windows Server. If everything is set up correctly Splunk will have 2 hosts that is pulling data.
  
![VirtualBox_Splunk_07_10_2024_14_09_16](https://github.com/user-attachments/assets/bba7605a-5bd6-4088-bdbe-fae2de1d644b)

*Ref 2: Setting up Static IP on Splunk Server*
  
![VirtualBox_Splunk_07_10_2024_17_32_35](https://github.com/user-attachments/assets/c3064102-bc0a-465d-9bec-1424e103a3ef)

*Ref 3: Installing Spunk onto the Splunk Server*
   
![VirtualBox_Splunk_07_10_2024_17_37_41](https://github.com/user-attachments/assets/e5f28e52-efda-4fe5-9f88-abd698c37d9c)

*Ref 4: Configuring the Splunk server to start up Slpunk everytime the VM is rebooted*

![VirtualBox_Windows 10_08_10_2024_14_04_15](https://github.com/user-attachments/assets/3f8eddff-6567-4a6d-84c9-8efdc7f551d2)

 *Ref 5: Screen that you will have if both Windows Target and Windows Server have Splunk and Sysmon installed and giving data*

- The fourth step was to install and configure Active Directory onto the Windows Server, promote the AD to a Domain Contoller, and congfigure the target machine to join the new Domain. On the Windows Server Manager by using the add roles and features a role/feature based install was selected for the Windows server with the Active Directory Certification Services role. Then install the AD Domain services. Once done then promote the server to a domain controller and create one and create users for the domain. Then go over to the Windows 10 VM. Then change the computer name and join the Domain of mutende.local and make sure the DNS server is pointing to the Domain Contoller. Then join the Domain with the admin credentials. Then sign into the Domain with the credentials of Jenny Smith.

  ![VirtualBox_ADDCO1_08_10_2024_15_28_09](https://github.com/user-attachments/assets/09adec23-be71-453b-8592-5dc31a10a2c9)

  *Ref 6: Install for the AD Domain services*

  ![VirtualBox_ADDCO1_08_10_2024_15_54_21](https://github.com/user-attachments/assets/574ef0b7-ec62-4e83-bef7-dd26d7289657)

  *Ref 7: The new user for the Organizational Unit of IT*

  ![Screenshot(8)](https://github.com/user-attachments/assets/d338ba4a-578d-4725-a1f0-d5a84f90b5f7)

 *Ref 8: Joining the Domain*

 -The fifth and final part is use Kali to preform a Brute Force Attack on the Domain users and view telemetry via Splunk.
 
 ![Screenshot(9)](https://github.com/user-attachments/assets/03685e4a-5b9c-4718-8438-8f80b741f689)

 *Ref 9: Setting up Static IP on Splunk Server*
   

