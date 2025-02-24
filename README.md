# ADB (Android Debug Bridge)

ADB (Android Debug Bridge) is a versatile command-line tool that allows developers and power users to communicate with Android devices from a computer. It enables debugging, file transfer, app installation, shell access, and more.

## 📌 Features

- Connect and control Android devices via USB or Wi-Fi
- Install and uninstall applications
- Access the device shell for debugging
- Transfer files between a PC and an Android device
- Capture screenshots and screen recordings
- Reboot and recover device functions
- Bypass bloatware and uninstall system apps

## 🚀 Installation

### **Windows**
1. Download the ADB Platform Tools from [Google's official site](https://developer.android.com/studio/releases/platform-tools).
2. Extract the ZIP file into a folder (e.g., `C:\adb`).
3. Open **Command Prompt** and navigate to the folder:  
   ```sh
   cd C:\adb
   ```
4. Test ADB installation by running:
   ```sh
   adb devices
   ```

### **Mac & Linux**
1. Open the terminal and install ADB using:
   ```sh
   brew install android-platform-tools  # For Mac (Using Homebrew)
   sudo apt install adb  # For Linux (Debian-based)
   ```
2. Verify installation:
   ```sh
   adb version
   ```

## 🔧 Usage

### **Enable Developer Mode & USB Debugging**
1. Go to **Settings > About Phone**.
2. Tap **Build Number** seven times to enable **Developer Options**.
3. Go to **Settings > Developer Options** and enable **USB Debugging**.

### **Basic Commands**
#### 1️⃣ Check Connected Devices
```sh
adb devices
```

#### 2️⃣ Access Device Shell
```sh
adb shell
```

#### 3️⃣ Install APK
```sh
adb install app.apk
```

#### 4️⃣ Uninstall App
```sh
adb uninstall com.example.app
```

#### 5️⃣ Transfer Files
- **Send file to device:**
  ```sh
  adb push file.txt /sdcard/
  ```
- **Retrieve file from device:**
  ```sh
  adb pull /sdcard/file.txt .
  ```

#### 6️⃣ Reboot Device
```sh
adb reboot
```

#### 7️⃣ Disable or Remove System Apps (Caution ⚠️)
- **Disable:**
  ```sh
  adb shell pm disable-user --user 0 com.android.example
  ```
- **Uninstall:**
  ```sh
  adb shell pm uninstall --user 0 com.android.example
  ```

## 📜 License
This project is licensed under the [MIT License](LICENSE).

## 🤝 Contribution
Feel free to open **issues** or submit **pull requests** if you have improvements or bug fixes.

## 🌟 Support
If you find this useful, don't forget to **star ⭐ the repository**!

---

Happy debugging! 🛠️
