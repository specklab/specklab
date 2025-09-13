# 👋 Hallo, ich bin Dominik

Umschüler **Fachinformatiker Systemintegration** – mit Fokus auf  
**Linux, Netzwerke, Virtualisierung, Container & Automatisierung**.  
Ich dokumentiere meine Lernprojekte praxisnah und prüfungsorientiert.  

---

## 🔧 Core Skills
![Linux](https://img.shields.io/badge/Linux-Debian-blue?logo=debian)
![Networking](https://img.shields.io/badge/Networking-DNS%2FDHCP%2FVPN-green)
![Proxmox](https://img.shields.io/badge/Proxmox-VE-orange?logo=proxmox)
![Docker](https://img.shields.io/badge/Docker-Compose-blue?logo=docker)
![Ansible](https://img.shields.io/badge/Ansible-Automation-red?logo=ansible)
![TrueNAS](https://img.shields.io/badge/Storage-TrueNAS-blue?logo=truenas)
![GitHub Actions](https://img.shields.io/badge/CI%2FCD-GitHub%20Actions-black?logo=githubactions)

---

## 📚 Projekte & Lernziele
- 🏠 [Homelab „Lab-Infra 1.0“](https://github.com/specklab/homelab)  
  → DNS/DHCP, Proxmox, TrueNAS, Nextcloud, Reverse Proxy, Mailserver, NetBox  

- 📦 [Ansible Homelab](https://github.com/specklab/ansible-homelab)  
  → Erste Playbooks: User & SSH-Hardening, Apache vHosts  

- 📝 [Skill- und Projekt-Datenbanken](https://github.com/specklab/notion-export)  
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

**Schema:** Symptom → Analyse → Lösung → Ergebnis

- **SSH-Hardening:** Kein Zugriff nach Config-Änderung → über Proxmox-Konsole `sshd_config.bak` zurückgespielt, danach schrittweise getestet.  
- **Docker-Port-Kollision:** Apache und Container blockierten denselben Port → Port-Plan erstellt, Dienste über Reverse Proxy erreichbar gemacht.  
- **iSCSI-Backup:** Nach Reboot war `/dev/sdb` nicht verfügbar → auf `/dev/disk/by-path/` umgestellt, Backup-Skript robuster gemacht.  
- **Mailserver TLS:** Thunderbird warnte vor Zertifikat → mit `openssl s_client` geprüft, SAN ergänzt, Zertifikat neu erstellt.  

---

## 📸 Screenshots (Block 2 – Netz & Core)
- ![Proxmox Login](docs/screens/block2_proxmox_login.png)  
  *Proxmox erreichbar unter https://proxmox.lab.local:8006*

- ![DNS Test mit dig](docs/screens/block2_dns_dig.png)  
  *BIND9 löst proxmox.lab.local korrekt auf → 192.168.10.10*

- ![DHCP Lease Windows Client](docs/screens/block2_dhcp_lease.png)  
  *Windows-Client erhält Lease aus 192.168.10.50–150*

---

## 📸 Screenshots (Block 4 – Web & Nextcloud)
- ![Nextcloud Login](docs/screens/block4_nextcloud_login.png)  
  *Nextcloud läuft mit HTTPS und self-signed Zertifikat*

---

## 📸 Screenshots (Block 5 – Docker, Proxy & Dokumentation)
- ![Portainer Dashboard](docs/screens/block5_portainer_dashboard.png)  
  *Portainer-UI für Container-Management*

- ![NetBox Übersicht](docs/screens/block5_netbox_overview.png)  
  *NetBox dokumentiert Devices, IPs und Services*

---

## 🎯 Zielbild
- **Prüfungsprojekt IHK** → voll dokumentiertes Homelab  
- **Portfolio für Bewerbungen** → praxisnahe Beispiele, Troubleshooting & Automatisierung  
