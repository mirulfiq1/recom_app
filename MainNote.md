# Recommender System

## Setup Environment

### 1. Conda 
- Download Anaconda from https://www.anaconda.com/download
- Install for your user account
- Verify installation: `conda --version`
- Initialize Conda for bash/Unix commands:
```bash
# Open Anaconda Prompt as Administrator
conda init bash
```
- Create and activate a new environment:
```bash
# Create new environment
conda create --name recom_env python=3.9
# Activate the environment
conda activate recom_env
```

### 2. Chocolatey
```powershell
# Run PowerShell as Administrator
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
- Verify installation: `choco --version`

### 3. Node.js
1. Install using Chocolatey:
```powershell
# Run PowerShell as Administrator
choco install nodejs.install -y
```

2. Close and reopen PowerShell/Terminal

3. Verify installation:
```bash
# Using bash terminal
node --version
npm --version
```

4. If still getting errors:
   - Check System Environment Variables:
     1. Press `Windows + R`
     2. Type `sysdm.cpl`
     3. Go to "Advanced" tab
     4. Click "Environment Variables"
     5. Under "System Variables", find "Path"
     6. Click "Edit"
     7. Add these paths if missing:
        - `C:\Program Files\nodejs\`
        - `%AppData%\npm`
     8. Click "OK" on all windows
     9. Restart VS Code

5. Alternative installation method:
   - Download Node.js directly from https://nodejs.org/
   - Choose LTS version
   - Run installer
   - Ensure "Add to PATH" is checked during installation

### 4. React Setup (After Node.js is working)
```bash
# Using bash terminal
npx create-react-app client --template typescript
cd client
npm start
```

### 5. Setting up Git Bash (Optional)
If you prefer using Git Bash for Unix-like commands:
```bash
# Install Git for Windows (includes Git Bash)
choco install git -y

# Configure Git Bash as default terminal in VS Code
# 1. Press Ctrl + Shift + P
# 2. Type "Select Default Profile"
# 3. Choose "Git Bash"
# 4. Open new terminal with Ctrl + `
```