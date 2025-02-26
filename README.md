# Wazuh-Installation-and-Agent-deployment-lab
# 🚀 Installing Wazuh in Ubuntu (VM)

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



For further customization and agent deployment, refer to [Wazuh Documentation](https://documentation.wazuh.com/).

