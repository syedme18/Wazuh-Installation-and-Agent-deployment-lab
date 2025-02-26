# Wazuh-Installation-and-Agent-deployment-lab
## 🚀 Installing Wazuh in Ubuntu (VM)

## 📌 Introduction
**Wazuh** is a free, open-source security system that provides **Extended Detection and Response (XDR)** and **Security Information and Event Management (SIEM)** functionality. It helps businesses monitor, detect, and respond to threats across endpoints, cloud environments, and on-premises infrastructure.

---

## 🖥️ Installing Ubuntu in a Virtual Machine (VMware)
### 🔗 Download Ubuntu ISO
Click [here](https://ubuntu.com/download/desktop) to download the Ubuntu ISO file.

### ⚙️ Setting Up Ubuntu in VMware
1. Open **VMware** and click on **New Virtual Machine**.
   
   ![1](https://github.com/user-attachments/assets/53d373ef-d5b4-4dd0-919b-5c3e75fb5236)


2. Select the downloaded **Ubuntu ISO file** and click **Next**.
   
   <img width="346" alt="2" src="https://github.com/user-attachments/assets/02f5cb7c-2bd1-444c-9825-cbd69bec3ded" />




3. Enter a **name, username, and password**, then click **Next**.
   
![3](https://github.com/user-attachments/assets/501aee77-452d-4f6a-9d8a-c1a9a1ae9c19)


4. Name your VM and choose the storage **location**.<br>
   <img width="338" alt="4" src="https://github.com/user-attachments/assets/62d6e027-093b-417a-91ca-a22ea4478ed2" />

   

5. Set **maximum disk capacity**, click **Next**, review settings, and **Finish**.
   
   <img width="350" alt="5" src="https://github.com/user-attachments/assets/779aed36-952c-4db8-897c-512fb85572aa" />


6. The newly created **Ubuntu Virtual Machine** will appear in the list.
   
   ![6](https://github.com/user-attachments/assets/699e1926-d8f2-4fdd-ac57-5b5cd06352df)


7. **Power on** the Ubuntu VM and follow installation steps if required.

---

## 🛠️ Installing Wazuh in Ubuntu Virtual Machine

### 🔹 **Installation Overview**
To install Wazuh, follow **three main steps**:
1. **Install Wazuh Indexer**
2. **Install Wazuh Server**
3. **Install Wazuh Dashboard**

*(Wazuh Agent will be deployed on endpoints separately.)*

### 🔄 **Update & Upgrade System**
Before installing Wazuh, update your system:
```sh
sudo apt update && sudo apt upgrade -y
```

### 📥 **One-Command Installation**
To install **Indexer, Server, and Dashboard** in a single command, run:
```sh
curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh && sudo bash ./wazuh-install.sh -a -i
```

![7](https://github.com/user-attachments/assets/ec44558d-0e41-4d54-b405-96e7d9de7456)


### 📌 **Accessing Wazuh Dashboard**
1. Once installation completes, the terminal will display **username and password**.
   
  ![8](https://github.com/user-attachments/assets/d99c35e3-3c34-4b39-a903-558ce7c4979a)


2. Open a **web browser** and enter the **VM's IP address** or the **link provided** in the terminal.
   
  ![9](https://github.com/user-attachments/assets/f8220c43-7a71-439f-afcc-285b9013ef48)


3. Enter the **username and password** from the terminal.
   
  ![10](https://github.com/user-attachments/assets/c043fabe-291c-41b5-af1c-2667cf08aaee)


4. You will now see the **Wazuh Dashboard**.
   
  ![11](https://github.com/user-attachments/assets/b425262d-fb9e-4776-95dc-fcbbdbfc8214)

   # Deploying Wazuh Agent in Malware Analysis VM

## Overview
This document provides step-by-step instructions for deploying a Wazuh agent in a malware analysis virtual machine (VM). Follow these steps carefully to ensure a successful deployment.

## Steps to Deploy Wazuh Agent

### 1. Add Agent from Home Screen
- Navigate to the Wazuh home screen.
- Click on **Add Agent**.  
  ![12](https://github.com/user-attachments/assets/eeb7122e-22bb-4445-8ddd-37fe494f7d7c)


### 2. Select Operating System
- Choose the appropriate operating system of the endpoint where the Wazuh agent will be installed.

### 3. Configure Server Details
- Enter the **IP address** of the Wazuh server.
- Assign an **agent name** to help identify the endpoint later.  
  


https://github.com/user-attachments/assets/0c0d1809-1ced-496f-be17-6154242f971a


### 4. Assign Agent Group
- Keep the existing group as **default**.

### 5. Generate Installation Command
- Wazuh will generate a command to run on the endpoint.  
  ![14](https://github.com/user-attachments/assets/18e6732c-f87c-43da-be88-b8d0ed596279)


### 6. Run Command on Endpoint
- Open **PowerShell as Administrator** on the endpoint.
- Copy and paste the generated command.
- The command will start writing a web request; wait until it completes.  
  

https://github.com/user-attachments/assets/4801dcf3-79a6-49ad-a87d-5901b0ec22d6



### 7. Run Second Command
- Copy and paste the second command in PowerShell on the endpoint.  
  


https://github.com/user-attachments/assets/12aafe73-66e2-4b41-ad4a-e65d2447d653


### 8. Verify Deployment
- Once the process is complete, the agent will appear in the **Agent section** as **Active**.  
 ![17](https://github.com/user-attachments/assets/a6ee6acc-9221-4d02-b6dd-fa0fb2999b23)


## Conclusion
By following these steps, you have successfully deployed the Wazuh agent on your malware analysis VM. The agent should now be actively monitoring the endpoint and sending data to the Wazuh server.





For further customization and agent deployment, refer to [Wazuh Documentation](https://documentation.wazuh.com/).

