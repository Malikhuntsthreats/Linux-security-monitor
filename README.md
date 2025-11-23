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
