# Linux Security Monitor
A lightweight Linux security automation tool that detects suspicious system changes in real time.  
Built with Python and designed for hands-on SOC and Incident Response learning.

---

## 🔥 Overview
This project continuously monitors critical Linux files for unauthorized modifications such as:

- New user accounts being added
- Privilege escalation (user added to sudo group)
- Cron job modifications
- System configuration changes

Every detection is logged to:

/var/log/linux_security_monitor.log

and printed live in the terminal.

---

## ⚙️ Features
- ✔ Real-time file integrity monitoring  
- ✔ Detects new users added  
- ✔ Detects privilege escalation  
- ✔ Detects cron file changes  
- ✔ Custom alert logging  
- ✔ Optional Discord or Email alerting  

---

## 📁 Files Monitored
- **/etc/passwd** – user accounts  
- **/etc/group** – groups / sudo  
- **/etc/crontab** – system-wide cron jobs  

---

**Monitor Running:**  
![](images/monitor_running.png)

**User Added Detected:**  
![](images/user_added.png)

**Cron Change Detected:**  
![](images/cron_detected.png)

---

📸 Screenshots

1️⃣ Creating the Project Directory

Created /opt/security-labs using mkdir.

![]([![](image/VirtualBox_Security2_#1.png90)

2️⃣ Opening the Script with Nano

Used sudo nano to create and edit the automation script.

![](image/VirtualBox_Security2_#2.png)

3️⃣ Adding the Python Detection Code

Pasted the full monitoring code into the nano editor.

![](image/VirtualBox_Security2_#3.png)

4️⃣ Activating Script Permissions

Applied sudo chmod to make the script executable.

![](image/VirtualBox_Security2_#4.png)

5️⃣ Running the Monitoring Script

Executed the script using sudo python3.

![](image/VirtualBox_Security2_#5.png)

6️⃣ Script Monitoring Loop Active (Overview of Code)

The script begins watching key system files and shows baseline + monitoring loop.

![](image/VirtualBox_Security2_#7.png)

7️⃣ Initial Monitoring Output

Real-time alerts appear as the script detects system changes.

![](image/VirtualBox_Security2_#9.png)

8️⃣ Adding a New Test User

Used sudo adduser test124 to simulate suspicious system activity.

![](image/VirtualBox_Security2_#10.png)

9️⃣ New User Successfully Added

Ubuntu confirms creation of the new user.

![](image/VirtualBox_Security2_#11.png)

🔟 Automated Alert Output

The detection script automatically logs the user creation event.

![](image/VirtualBox_Security2_#12.png)

## 🧠 Skills Demonstrated
- Detection engineering  
- IR automation  
- SOC alert triage thinking  
- Linux file integrity monitoring  
- Python scripting  
- Log analysis  

---

## 🚀 How to Run

Make script executable:
```bash
sudo chmod +x linux_security_monitor.py

and printed live in the terminal.

---

## ⚙️ Features
- ✔ Real-time file integrity monitoring  
- ✔ Detects new users added  
- ✔ Detects privilege escalation  
- ✔ Detects cron file changes  
- ✔ Custom alert logging  
- ✔ Optional Discord or Email alerting  

---

## 📁 Files Monitored
- **/etc/passwd** – user accounts  
- **/etc/group** – groups / sudo  
- **/etc/crontab** – system-wide cron jobs  

---

## 📸 Screenshots

**Monitor Running:**  
![](images/monitor_running.png)

**User Added Detected:**  
![](images/user_added.png)

**Cron Change Detected:**  
![](images/cron_detected.png)

---

## 🧠 Skills Demonstrated
- Detection engineering  
- IR automation  
- SOC alert triage thinking  
- Linux file integrity monitoring  
- Python scripting  
- Log analysis  

---

## 🚀 How to Run

Make script executable:
```bash
sudo chmod +x linux_security_monitor.py
sudo python3 linux_security_monitor.py
import smtplib

def email_alert(message):
    server = smtplib.SMTP("smtp.gmail.com", 587)
    server.starttls()
    server.login("YOUR_EMAIL", "YOUR_APP_PASSWORD")
    server.sendmail("YOUR_EMAIL", "RECIPIENT_EMAIL", message)
    server.quit()

👤 Author
Malik Lewis
Cybersecurity | SOC | Detection Engineering
