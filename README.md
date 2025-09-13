# Hi, ich bin Dominik 👋

**Fachinformatiker Systemintegration (i. A.)**  
Ich verbinde Systemintegration mit naturwissenschaftlicher Anwendung.

Linux · Netzwerke · Automatisierung · Data Science · Open Source

Ich entwickle automatisierte IT-Projekte mit Fokus auf Datenerfassung 
# 👋 Hallo, ich bin Dominik

Umschüler **Fachinformatiker Systemintegration** – mit Fokus auf  
**Linux, Netzwerke, Virtualisierung, Container & Automatisierung**.  
Ich dokumentiere meine Lernprojekte praxisnah und prüfungsorientiert.  

---

## 🔧 Skills (Auswahl)
![Linux](https://img.shields.io/badge/Linux-Debian-blue?logo=debian)
![Networking](https://img.shields.io/badge/Networking-DNS%2FDHCP%2FVPN-green)
![Proxmox](https://img.shields.io/badge/Proxmox-VE-orange?logo=proxmox)
![Docker](https://img.shields.io/badge/Docker-Compose-blue?logo=docker)
![Ansible](https://img.shields.io/badge/Ansible-Automation-red?logo=ansible)
![GitHub](https://img.shields.io/badge/Git-GitHub-lightgrey?logo=git)

---

## 📚 Projekte & Lernziele
- 🏠 [Homelab „Lab-Infra 1.0“](https://github.com/deinusername/homelab)  
  → DNS/DHCP, Proxmox, TrueNAS, Nextcloud, Reverse Proxy, Mailserver, NetBox  

- 📦 [Ansible Homelab](https://github.com/deinusername/ansible-homelab)  
  → Erste Playbooks: User & SSH-Hardening, Apache vHosts  

- 📝 [Skill- und Projekt-Datenbanken](https://github.com/deinusername/notion-export)  
  → Dokumentation meiner Lernfortschritte mit Notion-Integration  

---

## 🧭 Selbstreflexion & Entwicklung

Ein wichtiges Ziel meiner Arbeit ist es, **aus Fehlern zu lernen** und systematisch besser zu werden.  
Ein Beispiel aus meinem Homelab:

### 🖧 Projekt: DNS & Core Services (Block 2)
- **Ausgangslage:** Der Windows-Client bekam keine DNS-Auflösung, obwohl BIND9 auf SRV1 lief.  
- **Fehlerbild:** `dig proxmox.lab.local` lieferte *SERVFAIL*.  
- **Analyse:** Mit `named-checkzone` stellte ich fest, dass der Zonen-Serial nicht hochgezählt worden war.  
- **Lösung:** Zonenfile korrigiert, Serial erhöht (YYYYMMDDnn), danach Reload mit `systemctl reload bind9`.  
- **Ergebnis:** DNS funktionierte sofort, Proxmox war über FQDN erreichbar.  
- **Learnings:**  
  - Kleine Details (Serial) können kritische Auswirkungen haben.  
  - Strukturiertes Troubleshooting spart Zeit: **Symptom → Hypothese → Test → Fix → Verifikation**.  
  - Fehler dokumentieren = später schneller lösen.  

👉 Genau solche Erfahrungen steigern meine **Selbstständigkeit, Sorgfalt und Problemlösungskompetenz**.

---

## 🔧 Troubleshooting Highlights

Weitere typische Probleme & Lösungen aus meinem Homelab:

- **SSH-Hardening:** Kein Zugriff nach Config-Änderung → über Proxmox-Konsole `sshd_config.bak` zurückgespielt, danach Schrittweise getestet.  
- **Docker-Port-Kollision:** Apache und Container blockierten denselben Port → Port-Plan erstellt, Dienste über Reverse Proxy erreichbar gemacht.  
- **iSCSI-Backup:** Nach Reboot war `/dev/sdb` nicht verfügbar → auf `/dev/disk/by-path/` umgestellt, Backup-Skript robuster gemacht.  
- **Mailserver TLS:** Thunderbird warnte vor Zertifikat → mit `openssl s_client` geprüft, SAN ergänzt, Zertifikat neu erstellt.  

---

## 🎯 Zielbild
- **Prüfungsprojekt IHK** → voll dokumentiertes Homelab  
- **Portfolio für Bewerbungen** → praxisnahe Beispiele, Troubleshooting & Automatisierung  
