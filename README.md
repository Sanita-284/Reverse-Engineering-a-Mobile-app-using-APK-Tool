# 🔍 Reverse Engineering a Mobile App using APKTool

A mini project on Android mobile application security analysis through reverse engineering techniques.

> Mini Project — Department of Computer Science & Engineering (Cyber Security)  
> JAIN Deemed-to-be University, Bengaluru | April 2025

---

## 📌 Overview

This project demonstrates mobile security threat analysis by creating and reverse engineering a malicious Android application named **"Happening Around the City"**.

The application simulates malicious behavior by displaying false event information while secretly attempting to access sensitive user information.

Using **APKTool**, the APK was decompiled and statically analyzed to uncover:

- Hidden vulnerabilities
- Unauthorized data access attempts
- Dangerous permissions
- Malicious JavaScript code
- Social engineering techniques

The project highlights how reverse engineering can be used to identify security threats before they impact end users.

---

## 👨‍💻 Authors

| Name | Register No. |
|--------|------------|
| Abdul Hanooq Majeed | 23BTRCC003 |
| Sanita | 23BTRCC034 |

**Project Guide:** Dr. Harinee S  
*Assistant Professor*

**Institution:** JAIN Deemed-to-be University, Bengaluru

**Department:** Computer Science & Engineering (Cyber Security)

**Year:** April 2025

---

## 🎯 Objectives

- Understand Android mobile security threats
- Learn APK reverse engineering techniques
- Develop a malicious hybrid application for analysis
- Perform static APK analysis using APKTool
- Detect unauthorized access to user data
- Study cyber forensic investigation methods
- Demonstrate real-world mobile attack scenarios

---

## 🛠️ Tech Stack

| Category | Tools / Technologies |
|-----------|--------------------|
| App Development | Ionic Framework, JavaScript, TypeScript |
| Build Tools | Android Studio, Gradle |
| Reverse Engineering | APKTool 2.11.1 |
| Static Analysis | Visual Studio Code |
| Runtime | Java JDK 17, Node.js |
| Operating System | Windows 10 (64-bit) |

---

## 📁 Project Structure

```text
APK-Reverse-Engineering/
│
├── apktool.jar
├── apktool.bat
├── HappeningAroundTheCity.apk
│
├── Decompiled_Output/
│   ├── AndroidManifest.xml
│   ├── assets/
│   ├── res/
│   ├── smali/
│   └── unknown/
│
├── reports/
│   ├── findings.pdf
│   └── screenshots/
│
└── README.md
```

---

## ⚙️ Setup & Usage

### Prerequisites

- Java JDK 17+
- Node.js & npm
- APKTool
- Visual Studio Code
- Windows 10/11 or Ubuntu 20.04+

---

### Step 1 – Decompile APK

```bash
java -jar apktool.jar d HappeningAroundTheCity.apk
```

Windows:

```bash
apktool.bat d HappeningAroundTheCity.apk
```

---

### Step 2 – Inspect AndroidManifest.xml

Review dangerous permissions such as:

```xml
<uses-permission android:name="android.permission.READ_SMS"/>
<uses-permission android:name="android.permission.READ_CONTACTS"/>
<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE"/>
```

---

### Step 3 – Perform Static Analysis

Search for suspicious keywords:

```bash
grep -Ri "sms\|contact\|clipboard\|storage" .
```

Common targets include:

- SMS
- Contacts
- Clipboard
- Device Storage
- Background Services

---

### Step 4 – Generate Security Report

Document:

- Suspicious permissions
- File paths
- API calls
- Data collection behavior
- Evidence screenshots

---

## 🔬 Key Findings

### Hybrid Application Architecture

The application was developed using the **Ionic Framework** and relies heavily on JavaScript and TypeScript resources.

### Sensitive Data Access

Analysis revealed attempts to access:

- SMS Messages
- Contacts
- Clipboard Data
- Local Device Storage

### Excessive Permissions

The AndroidManifest.xml file requested multiple dangerous permissions beyond the application's stated functionality.

### Cordova Plugin Abuse

The application included:

```text
ionic-native-sms-retriever-plugin
```

which could be used for unauthorized SMS access.

### Social Engineering Design

The malicious functionality was hidden behind a legitimate-looking event discovery application.

---

## 📊 Analysis: Traditional vs Proposed Approach

| Criteria | Traditional APK Analysis | This Project |
|-----------|------------------------|-------------|
| Purpose | Metadata Review | Full Security Investigation |
| Decompilation | Limited | Complete APKTool Analysis |
| Hybrid App Support | Often Ignored | Fully Supported |
| JavaScript Analysis | Rarely Performed | Thorough Inspection |
| Findings | Basic Permissions | Detailed Threat Report |
| Threat Coverage | Low | High |

---

## 🧩 Modules

### 1. APKTool

Core decompilation engine responsible for:

- Decoding Android resources
- Extracting manifest files
- Reconstructing APK directory structure

---

### 2. Manifest Parser

Responsible for extracting:

- Package name
- Version information
- Application metadata
- Declared permissions

---

### 3. APKTool Batch Script

Provides a simplified execution environment on Windows systems.

Functions include:

- Java configuration
- APKTool execution
- Error handling

---

## 🚀 Future Enhancements

- [ ] Automated keyword scanning
- [ ] GUI-based APK analyzer
- [ ] Threat scoring engine
- [ ] Multiple APK batch analysis
- [ ] Certificate validation
- [ ] VirusTotal API integration
- [ ] MobSF integration
- [ ] JADX integration
- [ ] Dynamic analysis with Frida
- [ ] Dynamic analysis with Xposed Framework

---

## 📈 Learning Outcomes

This project helped demonstrate:

- Android reverse engineering fundamentals
- Mobile malware analysis
- Permission abuse detection
- Static application security testing
- Cyber forensic investigation techniques
- Secure mobile application design principles

---

## ⚠️ Disclaimer

This project was developed strictly for:

- Academic purposes
- Security research
- Educational demonstrations

The malicious application was created within a controlled environment solely to study mobile security threats.

Do **NOT** use these techniques on applications you do not own or have explicit authorization to analyze.

---

## 📚 References

The project references research papers and studies covering:

- APK Clone Detection (DroidCC)
- AI-Based Android Malware Detection
- Mobile Application Reverse Engineering
- IoT Security Analysis
- Obfuscation-Resistant Malware Analysis
- Android Permission Abuse Detection

For the complete bibliography, refer to the project report.

---

## 📄 License

This project was submitted as a Mini Project Report for partial fulfillment of the B.Tech Degree in Computer Science & Engineering (Cyber Security) at JAIN Deemed-to-be University.

You may use, modify, and extend this work for educational and research purposes with proper attribution.

---

> 🔍 Understanding Mobile Threats Through Reverse Engineering & Security Analysis
