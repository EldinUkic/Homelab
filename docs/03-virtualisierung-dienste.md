<h1 align="center">🧠 VIRTUALISIERUNG & DIENSTE</h1>

<p align="center">
  Übersicht über Hypervisor, Workload-Modelle und die aktuell auf der Homelab-Infrastruktur betriebenen Service-Kategorien.
</p>

<p align="center">
  <a href="../OVERVIEW.md">02-Homelab</a> / Docs / 03-Virtualisierung-Dienste
</p>

<p align="center">
  <a href="./01-infrastruktur.md">01 Infrastruktur</a> ·
  <a href="./02-network-vpn.md">02 Netzwerk & VPN</a> ·
  <a href="./03-virtualisierung-dienste.md">03 Virtualisierung & Dienste</a> ·
  <a href="./04-backup-monitoring-roadmap.md">04 Backup, Monitoring & Roadmap</a>
</p>

<hr style="border: none; height: 5px; background: linear-gradient(to right, transparent, #ffff, transparent); margin: 30px 0;">

<div style="background-color: #234; padding: 15px; border-left: 5px solid #007bff; border-radius: 5px;">
<strong>Status:</strong> ✅ Aktiv · 🔧 Geplant · ⚠️ In Arbeit<br>
Proxmox VE, VMs und LXC-Container sind laut Projektinfo im Einsatz. Mehrere Dienstekategorien laufen bereits, konkrete Einzelprodukte sind teilweise noch nicht bis ins Detail dokumentiert.
</div>

## 🖥️ Hypervisor-Plattform

<table style="width:100%; border-collapse: collapse;">
  <tr>
    <td width="58%" valign="top">
      <p>
        Die Virtualisierung basiert auf <strong>Proxmox VE</strong>. Damit ist das Homelab nicht nur eine Sammlung
        einzelner Bare-Metal-Installationen, sondern eine konsolidierte Plattform, auf der Workloads getrennt,
        wiederholbar und kontrolliert betrieben werden können.
      </p>
      <ul>
        <li><strong>Virtual Machines (VMs):</strong> für klassische isolierte Systeme</li>
        <li><strong>LXC Container:</strong> für leichte, effizient betriebene Workloads</li>
      </ul>
      <p>
        Die konkrete Verteilung, welche Dienste in VMs und welche in LXC laufen, ist in der Projektinfo noch
        nicht im Detail beschrieben und wird deshalb in dieser Dokumentation nur auf Ebene der Plattform und Diensteklassen dargestellt.
      </p>
    </td>
    <td width="42%" valign="top">
      <!-- FOTO: proxmox_dashboard.png - Proxmox-Übersicht mit Nodes, VMs und Containern -->
      <img src="../assets/proxmox_dashboard.png" alt="Proxmox-Übersicht mit laufenden virtuellen Maschinen und LXC-Containern">
      <p class="caption">Nachweis folgt</p>
    </td>
  </tr>
</table>

```text
Plattform

Proxmox VE
├── Virtual Machines
└── LXC Container
```

<hr style="border: none; height: 2px; background: linear-gradient(to right, transparent, #ffff, transparent); margin: 30px 0;">

## 🧩 Workload-Modell

<div style="display:flex; gap:20px; align-items:flex-start; flex-wrap:wrap;">
  <div style="flex:1; min-width:280px;">
    <table style="width:100%; border-collapse: collapse;">
      <tr>
        <th align="left">Workload-Typ</th>
        <th align="left">Zweck</th>
        <th align="left">Status</th>
      </tr>
      <tr>
        <td>VMs</td>
        <td>Isolierte Systeme, dedizierte Betriebsumgebungen</td>
        <td>✅ Aktiv</td>
      </tr>
      <tr>
        <td>LXC</td>
        <td>Ressourcenschonende Container-Workloads</td>
        <td>✅ Aktiv</td>
      </tr>
      <tr>
        <td>Docker-basierte Services</td>
        <td>Anwendungsdeployment innerhalb von Proxmox-Umgebungen</td>
        <td>✅ Aktiv</td>
      </tr>
      <tr>
        <td>Microservice-Grundlage</td>
        <td>Basis für eigene Anwendungen und skalierbare Services</td>
        <td>🔧 Geplant / im Ausbau</td>
      </tr>
    </table>
  </div>

  <div style="flex:1; min-width:280px;">
    <!-- FOTO: vm_lxc_overview.png - Übersicht der VMs und LXC-Container oder Ressourcenansicht -->
    <img src="../assets/vm_lxc_overview.png" alt="Übersicht laufender VMs und LXC-Container im Homelab">
    <p class="caption">Nachweis folgt</p>
  </div>
</div>

<hr style="border: none; height: 2px; background: linear-gradient(to right, transparent, #ffff, transparent); margin: 30px 0;">

## ☁️ Gehostete Dienste

### Private Cloud

<table style="width:100%; border-collapse: collapse;">
  <tr>
    <td width="58%" valign="top">
      <p>
        Im Homelab läuft eine Self-Hosted-Cloud-Lösung zur zentralen Dateiverwaltung. Der Zugriff ist laut
        Projektinfo von überall über VPN möglich. Das konkrete Produkt wird nur beispielhaft genannt und ist
        deshalb hier bewusst allgemein als private Cloud-Plattform beschrieben.
      </p>
      <ul>
        <li>Zentrale Dateiverwaltung</li>
        <li>Privater Zugriff über VPN</li>
        <li>Eigenkontrolle über Daten und Hosting</li>
      </ul>
    </td>
    <td width="42%" valign="top">
      <!-- FOTO: private_cloud_service.png - Cloud-Oberfläche oder Dateiverwaltung im Homelab -->
      <img src="../assets/private_cloud_service.png" alt="Self-hosted Cloud-Lösung für zentrale Dateiverwaltung im Homelab">
      <p class="caption">Nachweis folgt</p>
    </td>
  </tr>
</table>

### 🎬 Media Server

<table style="width:100%; border-collapse: collapse;">
  <tr>
    <td width="58%" valign="top">
      <p>
        Zusätzlich wird ein Media-Server für Verwaltung und Streaming von Medien im lokalen Netzwerk betrieben.
        Die konkrete Software wird in der Projektinfo nicht benannt und wird deshalb als Media-Server-Software beschrieben.
      </p>
      <ul>
        <li>Verwaltung von Medienbibliotheken</li>
        <li>Streaming innerhalb des lokalen Netzwerks</li>
        <li>Trennung zwischen Medien-Storage und System-Storage</li>
      </ul>
    </td>
    <td width="42%" valign="top">
      <!-- FOTO: media_server_ui.png - Oberfläche des Media-Servers oder Bibliotheksübersicht -->
      <img src="../assets/media_server_ui.png" alt="Media-Server im Homelab zur Verwaltung und Wiedergabe lokaler Inhalte">
      <p class="caption">Nachweis folgt</p>
    </td>
  </tr>
</table>

### 🐳 Container-Plattform

<table style="width:100%; border-collapse: collapse;">
  <tr>
    <td width="58%" valign="top">
      <p>
        Docker-basierte Services laufen innerhalb der Proxmox-Umgebung und dienen als Grundlage für das Deployment
        eigener Anwendungen. Aus der Projektinfo geht hervor, dass diese Schicht als Basis für spätere
        Microservices gedacht ist; die konkrete Platzierung in VM, LXC oder separatem Host wird in den Quelldaten nicht weiter aufgeschlüsselt.
      </p>
      <pre><code class="language-yaml">services:
  app:
    image: &lt;service-image&gt;
    restart: unless-stopped
    ports:
      - "&lt;published-port&gt;:&lt;container-port&gt;"
</code></pre>
    </td>
    <td width="42%" valign="top">
      <!-- FOTO: docker_services.png - Docker-Container oder Compose-gestützte Services im Betrieb -->
      <img src="../assets/docker_services.png" alt="Docker-basierte Services innerhalb der Proxmox-Umgebung">
      <p class="caption">Nachweis folgt</p>
    </td>
  </tr>
</table>

### 🔐 Reverse Proxy

<table style="width:100%; border-collapse: collapse;">
  <tr>
    <td width="58%" valign="top">
      <p>
        Der Reverse Proxy dient als zentraler Einstiegspunkt für Dienste und bildet die Grundlage für spätere
        Public Services. Genannt wird die Rolle, nicht jedoch das konkrete Produkt; Technologie und Routing-Regeln
        werden deshalb hier bewusst produktneutral beschrieben.
      </p>
      <ul>
        <li>Zentraler Einstiegspunkt für mehrere Services</li>
        <li>Routing und Verwaltung eingehender Anfragen</li>
        <li>Basis für später extern erreichbare Dienste</li>
      </ul>
    </td>
    <td width="42%" valign="top">
      <!-- FOTO: reverse_proxy_dashboard.png - Reverse-Proxy-Konfiguration oder Routing-Übersicht -->
      <img src="../assets/reverse_proxy_dashboard.png" alt="Reverse-Proxy als zentraler Einstiegspunkt für Homelab-Dienste">
      <p class="caption">Nachweis folgt</p>
    </td>
  </tr>
</table>

<hr style="border: none; height: 2px; background: linear-gradient(to right, transparent, #ffff, transparent); margin: 30px 0;">

## 📋 Service-Status

<table style="width:100%; border-collapse: collapse;">
  <tr>
    <th align="left">Service-Kategorie</th>
    <th align="left">Zweck</th>
    <th align="left">Technologie</th>
    <th align="left">Status</th>
  </tr>
  <tr>
    <td>Private Cloud</td>
    <td>Dateiverwaltung und privater Zugriff</td>
    <td>Self-hosted Cloud-Plattform</td>
    <td>✅ Aktiv</td>
  </tr>
  <tr>
    <td>Media Server</td>
    <td>Verwaltung und Streaming lokaler Medien</td>
    <td>Media-Server-Software</td>
    <td>✅ Aktiv</td>
  </tr>
  <tr>
    <td>Docker-Services</td>
    <td>Deployment eigener Anwendungen</td>
    <td>Docker</td>
    <td>✅ Aktiv</td>
  </tr>
  <tr>
    <td>Reverse Proxy</td>
    <td>Zentraler Einstiegspunkt für Dienste</td>
    <td>Reverse-Proxy-Dienst</td>
    <td>✅ Aktiv</td>
  </tr>
</table>

<hr style="border: none; height: 2px; background: linear-gradient(to right, transparent, #ffff, transparent); margin: 30px 0;">

<div style="background-color: #234; padding: 15px; border-left: 5px solid #007bff; border-radius: 5px;">
<strong>📊 FAZIT:</strong><br>
Die Virtualisierungsschicht mit Proxmox VE bildet das operative Zentrum des Homelabs und zeigt, dass Compute,
Isolation und Servicebetrieb strukturiert gedacht sind. Die Dienstelandschaft ist bereits breit genug, um
Dateiverwaltung, Medienbetrieb, Container-Deployment und zentrale Zugriffspfade abzubilden; die nächste sinnvolle
Verbesserung ist eine präzisere technische Feindokumentation der einzelnen Produkte und Platzierungen.
</div>

<hr style="border: none; height: 2px; background: linear-gradient(to right, transparent, #ffff, transparent); margin: 30px 0;">

<p align="center">
  <a href="./02-network-vpn.md">Zurück: 02 Netzwerk & VPN</a> ·
  <a href="./04-backup-monitoring-roadmap.md">Weiter: 04 Backup, Monitoring & Roadmap</a>
</p>
