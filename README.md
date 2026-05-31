<h1 align="center">HOMELAB</h1>

<p align="center">
  Dokumentation einer selbst aufgebauten Homelab-Umgebung mit Fokus auf Infrastruktur, Services, Segmentierung und Betrieb.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Status-Aktiv%20%2F%20Im%20Ausbau-blue?style=flat-square" />
  <img src="https://img.shields.io/badge/Hypervisor-Proxmox%20VE-E57000?style=flat-square" />
  <img src="https://img.shields.io/badge/VPN-WireGuard-88171A?style=flat-square" />
  <img src="https://img.shields.io/badge/Standorte-Serbien%20%2B%20Deutschland-2D7D46?style=flat-square" />
</p>

<div style="background-color: #234; padding: 15px; border-left: 5px solid #007bff; border-radius: 5px; color: #fff;">
<strong>WICHTIG:</strong> <br>
Es ist ein Work in Progress, es fehlen noch viele Sachen zu meinem Homelab, ebenfalls viele interne doku elemente die ich aus sicherheits Gründen nicht veröffentlichen kann.
</div>

<hr style="border: none; height: 3px; background: linear-gradient(to right, transparent, #555, transparent); margin: 30px 0;">

## 📑 Projektübersicht

Dieses Projekt dokumentiert den Aufbau und Betrieb meines eigenen, standortübergreifenden Homelabs. Ziel ist es nicht nur, einzelne Dienste zu hosten, sondern eine belastbare, zusammenhängende Systemlandschaft zu schaffen. Die Umgebung dient als praxisnahe Plattform für Infrastruktur-Design, Virtualisierung, Netzwerktechnik, Administration und strukturierte Fehleranalyse.

Hier werden reale Betriebsaufgaben wie automatisiertes Deployment, Netzwerksegmentierung, Absicherung, Backup-Strategien und das Management von Service-Abhängigkeiten unter professionellen Bedingungen umgesetzt.

### 🌐 Die Architektur im Überblick

Das Kernmerkmal dieses Setups ist eine **verteilte Architektur über zwei Länder**:

- **Standort Serbien:** Ein leistungsstarker Hauptserver im 24/7-Dauerbetrieb für die primären Dienste und Workloads.
- **Standort Deutschland:** Ein lokales Setup für die tägliche Verwaltung, Entwicklung und den sicheren Zugriff.

### 🛠️ Technisches Fundament

- **Virtualisierung:** Proxmox VE als solide Basis für Container (LXC) und VMs.
- **Standortvernetzung:** Sichere und performante Site-to-Site-Kopplung über WireGuard.
- **Storage:** Klar definierte und getrennte Storage-Rollen für Datenintegrität und Backups.

> **Der Anspruch dieses Projekts:** Diese Dokumentation dient als Nachweis dafür, dass hier keine vorgefertigten Tutorials blind nachgebaut wurden. Stattdessen zeigt sie das tiefere Verständnis für das Design, die Administration und die fortlaufende Pflege einer eigenständig betriebenen Enterprise-Infrastruktur im Kleinformat.

<hr style="border: none; height: 2px; background: linear-gradient(to right, transparent, #555, transparent); margin: 30px 0;">

## Kapitel

| #   | Kapitel                                                  | Inhalt                                           |
| --- | -------------------------------------------------------- | ------------------------------------------------ |
| 01  | [Infrastruktur](./docs/01-infrastruktur/1-Overview.md)   | Hardware beider Standorte, Storage, Systemrollen |
| 02  | [Netzwerk](./docs/02-network/overview.md)                | Topologie, WireGuard VPN, Firewall, DNS, WLAN    |
| 03  | [Virtualisierung](./docs/03-virtualisierung/overview.md) | Proxmox VE, VMs, LXC-Container, Deployment       |
| 04  | [Dienste](./docs/04-dienste/overview.md)                 | Core-Infrastruktur, Self-Hosted Apps             |
| 05  | [Operations](./docs/05-operations/overview.md)           | Backup-Strategie, Monitoring, Roadmap            |

## 🎞️ Vorschau

<table>
  <tr>
    <td align="center" width="33%">
      <img src="assets/rack_overview.jpg" width="240"><br>
      <b>📦 Netzwerkschrank</b><br>
      <sub>Sun Oracle 19" Rack</sub>
    </td>
    <td align="center" width="33%">
      <img src="assets/GroßesRZ_ServerInnen.jpg" width="240"><br>
      <b>🖥️ Server-Chassis</b><br>
      <sub>4 HE Servergehäuse</sub>
    </td>
    <td align="center" width="33%">
      <img src="assets/server_chassis.jpg" width="240"><br>
      <b>⚙️ Innenaufbau</b><br>
      <sub>Hardware & Komponenten</sub>
    </td>
  </tr>
</table>
