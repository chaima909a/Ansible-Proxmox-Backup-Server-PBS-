# 🔁 Backups Proxmox automatisés avec Ansible + PBS

Automatisation des **sauvegardes/restaurations** des VMs Proxmox via **Ansible** et **Proxmox Backup Server (PBS)**, avec **planification Cron** et **supervision Zabbix** (HA & DR). 【turn3file0】

## 🌐 Archi (résumé)
- Cluster Proxmox (3 nœuds) : 192.168.204.179 / .180 / .181  
- Stockage **NFS** pour migrations à chaud, **PBS** à 192.168.204.182 pour backups. 【turn3file0】
- Ansible exécute les playbooks (SSH), Zabbix supervise. 【turn3file0】

## ▶️ Usage rapide
1) Définir l’inventaire `inventory.ini`  
2) Lancer la sauvegarde : `ansible-playbook -i inventory.ini backup.yml`  
3) Planifier via Cron (exemple fourni)

## 🔧 Tech
Ansible, PBS, vzdump (snapshot, zstd, maxfiles), SSH, Cron, Zabbix. 【turn3file0】

✳️ Projet réalisé par Chayma ABIDI, 2025.
