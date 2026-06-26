# 🔐 Windows Event Viewer - User Login & Failed Password Log Analysis

## 📖 Project Overview

This project demonstrates how to monitor and analyze **Windows Security Logs** using **Windows Event Viewer** in a VirtualBox Windows environment.

The main objective is to investigate authentication events by identifying:

- ✅ Successful User Logins
- ❌ Failed Login Attempts
- 👤 User Authentication Activities
- 🛡️ Windows Security Event Logs

This project simulates a basic Security Operations Center (SOC) investigation where authentication events are analyzed for suspicious activities.

---

# 🎯 Objectives

- Understand Windows Event Viewer
- Learn Windows Security Logs
- Monitor Successful User Login
- Detect Failed Password Attempts
- Investigate Authentication Events
- Learn Important Windows Event IDs

---

# 🖥️ Lab Environment

| Component | Details |
|-----------|----------|
| Virtual Machine | Oracle VirtualBox |
| Operating System | Windows 10 / Windows 11 |
| Tool | Windows Event Viewer |
| Log Source | Windows Security Log |

---

# 📂 Event IDs Used

| Event ID | Description |
|----------|-------------|
| 4624 | Successful Logon |
| 4625 | Failed Logon |
| 4634 | User Logoff |
| 4647 | User Initiated Logoff |
| 4672 | Special Privileges Assigned |
| 4776 | Credential Validation |

---

# 🚀 Steps Performed

## Step 1

Open Event Viewer

```
Win + R

eventvwr.msc
```

---

## Step 2

Navigate to

```
Windows Logs
      ↓
   Security
```

---

## Step 3

Filter Security Logs

Click

```
Filter Current Log
```

Enter

```
4624,4625
```

Click **OK**

---

## Step 4

Generate Login Events

### Successful Login

Login using the correct password.

### Failed Login

Enter an incorrect password multiple times to generate Event ID 4625.

---

## Step 5

Analyze Event Details

Observe the following fields:

- Event ID
- Username
- Computer Name
- Time Created
- Logon Type
- Authentication Package
- Failure Reason
- Status Code
- Source Network Address

---

# 🔍 Event Analysis

## Event ID 4624

### Description

Successful user authentication.

### Key Information

- Username
- Logon Type
- Authentication Package
- Logon Process
- Process Name
- Source Network Address

### SOC Analysis

This event confirms that the user successfully authenticated to the Windows system.

---

## Event ID 4625

### Description

Failed login attempt.

### Key Information

- Username
- Failure Reason
- Status Code
- Sub Status Code
- Logon Type
- Source Network Address

### SOC Analysis

This event indicates that a login attempt failed due to invalid credentials or another authentication issue. Multiple failed login events may indicate a brute-force attack.

---

# 📸 Screenshots

Create a folder named **Screenshots** and add images for:

```
Screenshots/

├── security-log.png
├── filter-log.png
├── event-id-4624.png
├── event-id-4625.png
├── successful-login-details.png
└── failed-login-details.png
```

---

# 📊 Sample Investigation

| Event ID | Username | Status |
|----------|----------|--------|
| 4624 | User | Successful Login |
| 4625 | User | Failed Password Attempt |

---

# 🛠️ Skills Demonstrated

- Windows Event Viewer
- Windows Security Logs
- Authentication Monitoring
- Log Analysis
- Event ID Investigation
- Windows Security
- SOC Level-1 Investigation
- Incident Analysis
- Threat Detection Basics

---

# 📚 Learning Outcomes

After completing this project, I learned how to:

- Analyze Windows Security Logs
- Identify successful logins
- Detect failed password attempts
- Understand Windows Event IDs
- Investigate authentication events
- Perform basic SOC log analysis

---

# 🚀 Future Improvements

- PowerShell Log Collection
- Sysmon Integration
- Wazuh SIEM Integration
- Splunk Dashboard
- ELK Stack Visualization
- Brute Force Detection using PowerShell
- Automated Event Log Collection

---

# 📁 Project Structure

```
Windows-EventViewer-User-Login-Analysis/

│── README.md
│── REPORT.md
│── Screenshots/
│     ├── security-log.png
│     ├── filter-log.png
│     ├── event-id-4624.png
│     ├── event-id-4625.png
│     ├── successful-login-details.png
│     └── failed-login-details.png
```

---

# 📌 Conclusion

This project demonstrates how Windows Event Viewer can be used to monitor authentication events by analyzing Security Event IDs **4624** (Successful Logon) and **4625** (Failed Logon). Understanding these events helps security analysts detect unauthorized access attempts, investigate login activities, and strengthen Windows security monitoring.

---
