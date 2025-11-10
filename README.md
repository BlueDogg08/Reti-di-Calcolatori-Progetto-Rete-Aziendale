# 🖧 Progetto Reti di Calcolatori: Rete Aziendale

Questo repository contiene il progetto universitario per il corso **“Reti di Calcolatori: Protocolli”** dell’Università degli Studi di Perugia.

---

## 📘 Descrizione
Il progetto prevede la **progettazione e simulazione di una rete aziendale** comprendente 4 edifici e una DMZ, utilizzando **Cisco Packet Tracer**.  
La rete è stata sviluppata seguendo le specifiche fornite dal docente, con configurazione completa di:
- Router e Switch con protocollo di routing **RIP v2**  
- Server **DNS interno** e **DNS DMZ**  
- Server **Mail**, **Web** e **Backup**
- **Firewall interni ed esterni** per la protezione della rete
- Configurazione **Wi-Fi** per l’edificio D  
- Simulazione del funzionamento dei servizi e verifica con test di rete

---

## 🏢 Struttura della rete
| Edificio | N. Host | Server | Wi-Fi | Note |
|-----------|----------|---------|--------|------|
| A | 50 | DNS interno | ❌ | Rete interna |
| B | 50 | Backup | ❌ | Server salvataggi notturni |
| C | 100 | DNS, Mail, Web (DMZ) | ❌ | Cuore della rete |
| D | 50 | — | ✅ | Copertura wireless |

**DMZ:** collocata nell’edificio C, protegge i server esposti a Internet tramite doppio firewall (IN/OUT).

---

## ⚙️ Cablaggio
- Fibra ottica multimodale OM3 per connessioni tra router (backbone)  
- Cavi **STP Cat.6** e **Cat.5e** per dorsali interne  
- **UTP Cat.5e** per collegamenti ai terminali

---

## 🌐 Indirizzamento IP
- Rete principale: `192.164.0.0/16`
- Sottoreti:
  - A → `192.168.1.0/26`
  - B → `192.168.2.0/26`
  - C → `192.168.3.0/25`
  - D → `192.168.4.0/26`
  - DMZ → `192.168.5.0/29`
  - Backbone Router → `192.168.0.0/28`

---

## 🔒 Sicurezza
- Doppio firewall (IN e OUT) con politica **default deny**  
- Monitoraggio della rete e test di sicurezza con **Cisco Packet Tracer**  
- Protezione fisica dei server (backup e DMZ) con:
  - Accesso riservato
  - Sistemi anti-incendio e di raffreddamento
  - Videosorveglianza e allarme anti-intrusione

---

## 💻 File inclusi
- `Documentazione_AlunniSantoniAlessio_360481.pdf` → relazione completa del progetto  
- `Progetto_Rete_Aziendale.pkt` → simulazione su Cisco Packet Tracer  
- `README.md` → documento introduttivo (questo file)

---

## 🧾 Autore
**Alunni Santoni Alessio**  
Matricola: 360481  
Università degli Studi di Perugia – Dipartimento di Matematica e Informatica  
Corso: *Reti di Calcolatori – Protocolli*  

---

📅 **Anno Accademico:** 2024/2025  
🔗 **Docente:** Prof. Sergio Tasso
