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

- **Standort Serbien**
- **Standort Deutschland**

### 🛠️ Technisches Fundament

- **Virtualisierung:** Proxmox VE als solide Basis für Container (LXC) und VMs.
- **Standortvernetzung:** Sichere und performante Site-to-Site-Kopplung über WireGuard.
- **Storage:** Klar definierte und getrennte Storage-Rollen für Datenintegrität und Backups.

> **Der Anspruch dieses Projekts:** Diese Dokumentation dient als Nachweis dafür, dass hier keine vorgefertigten Tutorials blind nachgebaut wurden. Stattdessen zeigt sie das tiefere Verständnis für das Design, die Administration und die fortlaufende Pflege einer eigenständig betriebenen Enterprise-Infrastruktur im Kleinformat.

<hr style="border: none; height: 2px; background: linear-gradient(to right, transparent, #555, transparent); margin: 30px 0;">

## Tabel of Content

- [01. Infrastruktur](./docs/01-infrastruktur/1-Overview.md)
  - [1.1 Housing ](./docs/01-infrastruktur/1.1-Housing.md)
  - [1.2 Server Hardware](./docs/01-infrastruktur/1.2-Server_Hardware.md)
  - [1.3 Firewall Hardware](./docs/01-infrastruktur/1.3-Firewall_Hardware.md)
  - [1.4 Network Hardware](./docs/01-infrastruktur/1.4-Network‚_Hardware.md)
  - [1.5 Verkablungsplan](./docs/01-infrastruktur/1.5-Verkabungsplan.md)
  - [1.6 Storage Layout](./docs/01-infrastruktur/1.6-Storage_Layout.md)
- [02. Netzwerk](./docs/02-network/overview.md)
  - [2.1 Deutschland Network](./docs/02-network/2.1-Deutschland.md)
  - [2.2 Serbien Network](./docs/02-network/2.2-Serbien.md)
  - [2.3 VPN Konzept](./docs/02-network/2.3-VPN_Konzept.md)
- [03. Services](./docs/02-network/overview.md) 🚧Wird ergänzt
- [04. Umgesetzte Projekte](./docs/02-network/2.1-Deutschland.md)

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
