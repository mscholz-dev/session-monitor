# Session-Monitor Setup Guide 🚀

This guide will show you how to set up a monitoring service on your Debian-based Linux OS using a Bash script. This script allows you to monitor sessions on your PC and receive Discord notifications.

## 1. 📜 Create a notification log file

```bash
sudo touch /var/log/session-monitor.log
```

## 2. 📁 Move the service file to the systemd directory

```bash
sudo mv session-monitor.service /etc/systemd/system/session-monitor.service
```

## 3. 👑 Add root privileges to the service file

```bash
sudo chown root:root /etc/systemd/system/session-monitor.service
```

## 4. 📂 Move the Bash script to the shell script directory

```bash
sudo mv session-monitor /usr/local/sbin/session-monitor
```

## 5. 👑 Add root privileges to the Bash script

```bash
sudo chown root:root /usr/local/sbin/session-monitor
```

## 6. 🔒 Make the Bash script executable

```bash
sudo chmod +x /usr/local/sbin/session-monitor
```

## 7. 🚀 Enable this service to start automatically

```bash
sudo systemctl enable session-monitor.service
```

## 8. 🔗 Add your Discord webhook URL to the Bash script

```bash
sudo nano /usr/local/bin/session-monitor
```

## 9. 🔄 Reboot your system and monitor your Discord webhook channel

```bash
reboot
```

## Have fun! 🎉

If you encounter any issues or want to disable this service, here's how:

🛑 Disable the service from starting at the next boot.

```bash
sudo systemctl disable session-monitor.service
```

⏸️ Temporarily stop the service for this session.

```bash
sudo systemctl stop session-monitor.service
```

🔍 You can test the script by executing the following command:

```bash
session-monitor
```
