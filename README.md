# 🎬 yt-easy-bulk-edit
🚀 A command-line tool to **fetch, manage, and bulk-edit YouTube playlists and videos** using the **YouTube Data API v3**.

---

# This project is 🚧 *Under Development*

---

## 🎯 **Project Goal**
This tool automates **YouTube playlist management** by allowing users to:
- **Fetch & list playlists**
- **Retrieve videos from selected playlists**
- **(Upcoming) Bulk edit video titles, descriptions, privacy settings, etc.**

---

## 🛠 **Features**
✅ **Authenticate with YouTube API** (OAuth 2.0)  
✅ **Fetch & List Playlists** → [`list-playlist-ids.py`](list-playlist-ids.py)  
✅ **Fetch & Save Videos from Playlists** → [`list-playlist-videos.py`](list-playlist-videos.py)  
⏳ **(Upcoming) Bulk Edit Videos** → Modify **titles, descriptions, privacy settings**  

---

## ⚙️ **Tools & Technologies Used**
This project utilizes the following tools and technologies:
- **Programming Language:** Python 3
- **YouTube Data API v3** (for interacting with YouTube)
- **Google Cloud Console** (for API & OAuth setup)
- **OAuth 2.0 Authentication** (for secure API access)
- **Google API Client (`googleapiclient`)**
- **pip** (for managing Python dependencies)
- **Git & GitHub** (for version control & collaboration)
- **Ubuntu / WSL** (for development environment)
- **Shell/CLI** (for executing scripts)

---

## 🚀 **Project Setup**
### **Step 1: Clone the Repository**
```bash
git clone https://github.com/0xKatie/yt-easy-bulk-edit.git
cd yt-easy-bulk-edit
```

### **Step 2: Install Dependencies**
To run the scripts, you need to install the required Python packages.

Run the following command in your terminal:
```bash
pip install --upgrade google-auth google-auth-oauthlib google-auth-httplib2 google-api-python-client
```

#### **What This Does:**
- **`google-auth`** → Handles authentication with Google's APIs.
- **`google-auth-oauthlib`** → Manages OAuth 2.0 flow for user authentication.
- **`google-auth-httplib2`** → Supports authentication over HTTP.
- **`google-api-python-client`** → Provides access to the YouTube Data API v3.

#### **Verify Installation**
After installation, you can check if the packages were installed correctly by running:
```bash
pip list | grep google
```

If the packages are installed, you should see versions listed next to each.


### **Step 3: Set Up YouTube API Credentials**
To interact with the YouTube Data API, you need to **set up OAuth 2.0 authentication** in Google Cloud Console.

#### **1️⃣ Enable YouTube Data API v3**
1. Go to **[Google Cloud Console](https://console.cloud.google.com/)**
2. Create a new project (or select an existing one).
3. Navigate to **APIs & Services** → **Library**.
4. Search for **YouTube Data API v3** and click **Enable**.

#### **2️⃣ Create OAuth 2.0 Credentials**
1. Go to **APIs & Services** → **Credentials**.
2. Click **Create Credentials** → **OAuth Client ID**.
3. Select **"Desktop App"** as the application type.
4. Click **Create** and **Download JSON** (this file is needed for authentication).

#### **3️⃣ Move the `client_secrets.json` File**
- Rename the downloaded file to `client_secrets.json` (if it has a long name).
- Move it into your project folder:
```bash
mv ~/Downloads/client_secrets.json ~/yt-easy-bulk-edit/
```
