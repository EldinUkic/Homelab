<h1 align="center">💻 Kapitel 1: Infrastruktur Overview</h1>

<p align="center">

</p>

<p align="center">
  <a href="../../README.md">🏠 Hauptmenü</a> / <b>01-Infrastruktur</b> / 1-Overview
</p>

<hr style="border: none; height: 3px; background: linear-gradient(to right, transparent, #555, transparent); margin: 30px 0;">

## 🌐 Kapitel Übersicht

Dieses Kapitel dokumentiert das physische und logische Fundament meines gesamten Setups. Das primäre Ziel dieser Infrastruktur ist es nicht nur, Dienste bereitzustellen, sondern ein <strong>reales, standortübergreifendes Enterprise-Szenario</strong> abzubilden.

Hier wird im Detail aufgeschlüsselt, welche Hardware-Komponenten zum Einsatz kommen, warum genau diese Hardware ausgewählt wurde und wie die einzelnen Systeme logisch miteinander interagieren. Das Setup verteilt sich auf zwei Länder.

<hr style="border: none; height: 2px; background: linear-gradient(to right, transparent, #555, transparent); margin: 25px 0;">

## 🌍 Infrastruktur-Standorte

<p align="center">
  <img
    src="../../assets/standorte.png"
    alt="Infrastruktur-Standorte Übersicht"
    width="100%"
  >
</p>

Die Infrastruktur verteilt sich auf zwei physisch getrennte Standorte:

| Standort       | Beschreibung                                                                            |
| -------------- | --------------------------------------------------------------------------------------- |
| 🇷🇸 Serbien     | Virtualisierung, Storage, Netzwerk-Infrastruktur, Access Points & zentrale Dienste      |
| 🇩🇪 Deutschland | Firewall, VPN-Endpunkt, Monitoring, Entwicklung, Testing & lokale Infrastruktur-Dienste |

<hr style="border: none; height: 2px; background: linear-gradient(to right, transparent, #555, transparent); margin: 25px 0;">

## Inhalt dieses Kapitels

| #   | Datei                                                       | Inhalt                                                          |
| --- | ----------------------------------------------------------- | --------------------------------------------------------------- |
| 1.1 | [`1.1-Housing`](./1.1-Housing.md)                           | Gehäuse, Rack-Setup und physische Unterbringung der Hardware    |
| 1.2 | [`1.2-Server Hardware`](./1.2-Server_Hardware.md)           | Rechenknoten – CPU, RAM, Speicher und Rollen aller Server-Nodes |
| 1.3 | [`1.3-Firewall Hardware`](./1.3-Firewall_Hardware.md)       | Firewall-Appliances – Dell Wyse 3040 mit OPNsense               |
| 1.4 | [`1.4-Netzwerk Komponenten`](./1.4-Netzwerk_Komponenten.md) | Switches, Access Points und lokale Netzwerk-Endpunkte           |
| 1.5 | [`1.5-Verkalblungsplan`](./1.5-Verkablungsplan.md)          | Storage-Konzept, Datenträger-Zuordnung und Datensicherung       |
| 1.6 | [`1.5-Storage Layout`](./1.6-Storage_Layout.md)             | Storage-Konzept, Datenträger-Zuordnung und Datensicherung       |

<hr style="border: none; height: 2px; background: linear-gradient(to right, transparent, #555, transparent); margin: 25px 0;">

<h2>🔍 System-Matrix auf einen Blick</h2>

<table style="width:100%; border-collapse: collapse; margin-top: 15px;">
  <thead>
    <tr style="border-bottom: 2px solid #555;">
      <th align="left" style="padding: 8px;">Standort</th>
      <th align="left" style="padding: 8px;">System-Kategorie</th>
      <th align="left" style="padding: 8px;">Primärer Einsatzzweck</th>
      <th align="left" style="padding: 8px;">Betriebsmodell</th>
      <th align="left" style="padding: 8px;">Status</th>
    </tr>
  </thead>
  <tbody>
    <tr style="border-bottom: 1px solid #ddd;">
      <td style="padding: 8px;"><strong>🇷🇸 Serbien</strong></td>
      <td style="padding: 8px;">Proxmox-Node / Zentrales Rack-System</td>
      <td style="padding: 8px;">Flexible Virtualisierungsplattform für verschiedene Serverrollen</td>
      <td style="padding: 8px;">24/7 Dauerbetrieb</td>
      <td style="padding: 8px;">✅ Aktiv</td>
    </tr>
    <tr style="border-bottom: 1px solid #ddd;">
      <td style="padding: 8px;"><strong>🇩🇪 Deutschland</strong></td>
      <td style="padding: 8px;">Proxmox-Node / 24/7 Service-Server</td>
      <td style="padding: 8px;">Dauerhaft verfügbare Dienste, Monitoring & Infrastruktur-Services</td>
      <td style="padding: 8px;">24/7 Dauerbetrieb</td>
      <td style="padding: 8px;">✅ Aktiv</td>
    </tr>
    <tr style="border-bottom: 1px solid #ddd;">
      <td style="padding: 8px;"><strong>🇩🇪 Deutschland</strong></td>
      <td style="padding: 8px;">Proxmox-Node / Entwicklungs- und Testserver</td>
      <td style="padding: 8px;">Entwicklung, Tests, Experimente & temporäre Workloads</td>
      <td style="padding: 8px;">On-Demand</td>
      <td style="padding: 8px;">✅ Aktiv</td>
    </tr>
    <tr>
      <td style="padding: 8px;"><strong>🇩🇪 Deutschland</strong></td>
      <td style="padding: 8px;">Firewall-Appliance / OPNsense-Gateway</td>
      <td style="padding: 8px;">Netzwerksicherheit, Paketfilterung & VPN-Gateway (Dell Wyse 3040)</td>
      <td style="padding: 8px;">24/7 Dauerbetrieb</td>
      <td style="padding: 8px;">✅ Aktiv</td>
    </tr>
  </tbody>
</table>
