# 🧭 GenDaily Setup Guide

Welcome to the **GenDaily** setup guide — your quick start to running the **daily on-chain check-in dApp** built for the GenLayer ecosystem.

GenDaily lets you perform **one meaningful on-chain action per UTC day** and build streaks that reflect your consistency on the network.  
It’s lightweight, open-source, and designed to help new builders understand the **GenLayer transaction lifecycle** (from `Accepted` → `Finalized`).

---

## 🚀 What You’ll Learn

This guide shows how to:
- Set up the project on **Windows + WSL (Ubuntu)**
- Connect to **GenLayer StudioNet** (chainId `61999`)
- Run the app locally and perform your **daily check-in**

# 🧰 WSL Setup Guide (Windows Subsystem for Linux)

This guide helps you install and prepare **WSL (Windows Subsystem for Linux)** to run the **GenDaily** project on Windows smoothly.  
It covers everything from enabling WSL to installing Node.js, npm, and Git inside Ubuntu.

---

🪟 1. **Enable WSL on Windows**(skip to step 3 if already configure)
### Step 1. Open PowerShell as Administrator  
Press **Start → type "PowerShell" → Right-click → Run as Administrator**
### Step 2. Run the install command  
```wsl --install```

🐧 2. **Open Ubuntu (WSL)**
After reboot, open Ubuntu from the Start menu.
The first launch may take a few minutes and ask you to:
Create a UNIX **username**
Set a **password**

🔄 3. **Update and upgrade packages**
sudo apt update && sudo apt upgrade -y

⚙️ 4. **Install Node.js, npm, and Git**
```sudo apt install -y curl git```
```curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -```
```sudo apt install -y nodejs```

🧩 5. **Clone and prepare GenDaily**
```git clone https://github.com/ngh1105/GenDaily.git```
```cd GenDaily```
```npm install```

🧾 6. **Create environment file**
```nano .env.local```

Paste the text:
_NEXT_PUBLIC_GENLAYER_NETWORK=studionet
NEXT_PUBLIC_CONTRACT_ADDRESS=0x362DAaCBaca07c64E7C9fa32787A6c1F0001A076
NEXT_PUBLIC_APP_NAME="GenLayer Daily Check-in"_

Save and exit (Ctrl + O → Enter → Ctrl + X).

▶️ 7. **Run the project**
```npm run dev```
Open in your browser **http://localhost:3000**

🦊 8. **Connect MetaMask**
Add a new network manually:
Network name: **GenLayer StudioNet**
RPC URL: **https://studio.genlayer.com/api**
Chain ID: **61999**
Currency symbol: **GEN**

Connect your wallet when the app asks.
You’re ready to check in daily!
