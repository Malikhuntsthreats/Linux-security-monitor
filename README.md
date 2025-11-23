🛡️ Linux Security Monitor

A lightweight security automation script built on Ubuntu that detects suspicious system activity in real time without requiring a SIEM or SOAR platform.

This project watches critical Linux files and logs such as:

/etc/passwd → new users added or removed

/etc/group → privilege / sudo modifications

/etc/crontab → unauthorized scheduled tasks

Whenever a suspicious change is detected, the monitor:

✔ Logs it to /var/log/linux_security_monitor.log
✔ Prints a timestamped alert to the console
✔ Helps simulate real IR & detection engineering workflows

🚀 Features

Real-time file integrity monitoring

Detection of new user accounts

Detection of privilege escalation

Cron job monitoring

Alert logging

Simple Python design for learning IR automation

🧠 Skills Demonstrated

Detection engineering

Incident response logic

Security automation

Real Linux IR concepts

File integrity monitoring

Python scripting

System monitoring

Perfect for:

SOC Analyst resume

IR portfolio

Job applications

LinkedIn posts

GitHub experience

📂 How to Run
sudo python3 linux_security_monitor.py


Alerts will appear in:

/var/log/linux_security_monitor.log

📬 Optional: Send Alerts to Discord or Email

You can add a Discord webhook inside the alert() function:

import requests

WEBHOOK_URL = "YOUR_WEBHOOK_HERE"

def alert(message):
    ts = time.strftime("%Y-%m-%d %H:%M:%S")
    line = f"[{ts}] {message}"
    print(line)

    requests.post(WEBHOOK_URL, json={"content": line})


Or you can use smtplib for email alerts (I can add that for you too).

📜 License

MIT License.

🖊️ Author

Malik Lewis
Security Analyst • Detection Engineering • IR Automation

⭐ If you like this project, star the repo!
