# Session-Monitor Setup Guide 🚀

Ce guide vous montrera comment configurer un service de monitoring sur votre OS Linux sous Debiane avec un script bash qui vous permet de surveiller les sessions de votre PC et de recevoir des notifications Discord.

## 1. 📜 Créez un fichier journal pour les notifications

```bash
sudo touch /var/log/session-monitor.log
```

## 2. 📁 Déplacez le fichier de service vers le répertoire systemd

```bash
sudo mv session-monitor.service /etc/systemd/system/session-monitor.service
```

## 3. 👑 Ajoutez les privilèges root au fichier de service

```bash
sudo chown root:root /etc/systemd/system/session-monitor.service
```

## 4. 📂 Déplacez le script Bash vers le répertoire de scripts shell

```bash
sudo mv session-monitor /usr/local/sbin/session-monitor
```

## 5. 👑 Ajoutez les privilèges root au script Bash

```bash
sudo chown root:root /usr/local/sbin/session-monitor
```

## 6. 🔒 Rendez le script Bash exécutable

```bash
sudo chmod +x /usr/local/sbin/session-monitor
```

## 7. 🚀 Activez ce service pour qu'il démarre automatiquement

```bash
sudo systemctl enable session-monitor.service
```

## 8. 🔗 Ajoutez votre URL de webhook Discord au fichier Bash

```bash
sudo nano /usr/local/bin/session-monitor
```

## 9. 🔄 Redémarrez votre système et surveillez votre canal de webhook Discord

```bash
reboot
```

## Amusez-vous bien ! 🎉

Si vous rencontrez des problèmes ou souhaitez désactiver ce service, voici comment le faire :

🛑 Désactivez le service pour qu'il ne démarre pas au prochain démarrage.

```bash
sudo systemctl disable session-monitor.service
```

⏸️ Désactivez temporairement le service pour cette session

```bash
sudo systemctl stop session-monitor.service
```

🔍 Vous pouvez exécuter le script avec la commande suivante

```bash
session-monitor
```
