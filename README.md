# Counter-Strike WaRzOnE: Play with Friends on College Wi-Fi (2025 Guide)

#### NOTE: The first person aka host will have to download the zip file and extract it from this repository and then can share that via python http command (the python http command is just for faster download speeds so you dont waste lab-time setting up the game)

This guide will help you **set up, share, and play Counter-Strike WaRzOnE with friends on college Wi-Fi** despite network restrictions. We will use a **local file-sharing server** and **HLDS (Half-Life Dedicated Server)** to play multiplayer matches.

## **1. Download & Share Game Files**
Since college Wi-Fi blocks many sites, we will **share the game files directly** using a Python-based local file server.

### **A. Start File-Sharing Server (Python Method)**
1. **Install Python** (if not already installed):  
   Download and install Python from [python.org](https://www.python.org/downloads/).

2. **Open PowerShell or Command Prompt** and navigate to the game folder:
   ```powershell
   cd "C:\path\to\Counter-Strike WaRzOnE"
   ```
3. **Start a file-sharing server:**
   ```powershell
   python -m http.server 8000 --bind 0.0.0.0
   ```
   - This will start a local server on **port 8000**.
   - **Find your local IP**: Run this command in PowerShell:
     ```powershell
     ipconfig | findstr "IPv4"
     ```
   - **Example output:** `IPv4 Address: 192.168.1.5`
   - **Share this link with friends**:  
     ```
     http://192.168.1.5:8000
     ```
     Anyone connected to the same Wi-Fi can **download the game files** via browser.

4. **Download the game on another PC:**
   - Open a browser on the friend’s computer.
   - Enter `http://YOUR_LOCAL_IP:8000` (e.g., `http://192.168.1.5:8000`).
   - Click on **Counter-Strike WaRzOnE.zip** to download the game.
   - **Extract the ZIP file** after download is complete.

### **B. Alternative: Share via USB or External HDD**
If the network blocks file-sharing servers, **copy the game to a USB drive and share manually**.

---
## **2. Setup the Game**
1. **Extract the ZIP file** into a folder like `C:\Games\Counter-Strike WaRzOnE`.
2. Open the folder and run **CS16Launcher.exe**(which is inside the extracted zip file) to start the game.
3. **Go to Options > Multiplayer > Customize** and change your name.

---
## **3. Host a Local Multiplayer Server (HLDS Method)**
### HLDS is included in the zip file extract it and run it
To play on LAN (college Wi-Fi), we need to host a **Half-Life Dedicated Server (HLDS)**.

### **A. Start HLDS Server**
1. Open the **Counter-Strike WaRzOnE** folder.
2. Run **hlds.exe** (Half-Life Dedicated Server).
3. Configure the server:
    - Add preferred setting such as maps, starting money, etc.
4. Click **Start Server**.
5. **Find Your Server IP**
    - IP address will be written on that page

---
## **4. Join the Game (Friends’ PC Setup)**
1. Open **CS16Launcher.exe**.
2. Go to **Find Servers -> Favorites -> Favorites -> Add Server -> Add the server ip which was just created**.
3. If the server doesn’t appear:
   - Open the console (`~` key) and type:
     ```
     connect 192.168.1.5:27015
     ```
     (Replace with the actual host’s IP).

---
## **5. Fixing Common Issues**
### ❌ **Game doesn’t show in LAN Servers**
✅ Fix: Use the **console method** to manually connect:
```console
connect YOUR_SERVER_IP:27015
```

### ❌ **Connection Timed Out / Could Not Connect**
✅ Fix: Make sure **both players** are on the same Wi-Fi network.

### ❌ **HLDS Server Not Visible**
✅ Fix: Disable Windows Firewall temporarily.
- Open PowerShell as Admin and run:
  ```powershell
  netsh advfirewall set allprofiles state off
  ```
- **Turn it back on after playing**:
  ```powershell
  netsh advfirewall set allprofiles state on
  ```

---
## **6. Enjoy the Game! 🎮**
Now you and your friends can play Counter-Strike WaRzOnE on **college Wi-Fi!** 🚀

Made with love by 2nd Year B.Tech Cybersecurity 24-25 students
