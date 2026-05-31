<h1 align="center">💾 BACKUP, MONITORING & ROADMAP</h1>

<p align="center">
  Dokumentation von Datensicherheit, Wiederherstellungsstrategie, aktuellem Monitoring-Status sowie den nächsten Ausbauschritten des Homelabs.
</p>

<p align="center">
  <a href="../OVERVIEW.md">02-Homelab</a> / Docs / 04-Backup-Monitoring-Roadmap
</p>

<p align="center">
  <a href="./01-infrastruktur.md">01 Infrastruktur</a> ·
  <a href="./02-network-vpn.md">02 Netzwerk & VPN</a> ·
  <a href="./03-virtualisierung-dienste.md">03 Virtualisierung & Dienste</a> ·
  <a href="./04-backup-monitoring-roadmap.md">04 Backup, Monitoring & Roadmap</a>
</p>

<hr style="border: none; height: 5px; background: linear-gradient(to right, transparent, #ffff, transparent); margin: 30px 0;">

<div style="background-color: #5c4700; border-left: 6px solid #d4a017; padding: 14px 18px; margin: 20px 0; border-radius: 8px; color: #f8e7a1;">
<strong>Hinweis:</strong><br>
Ein grundlegendes Backup-Konzept ist bereits implementiert. Aktives Monitoring läuft laut Projektinfo derzeit noch nicht und ist als nächster Entwicklungsschritt vorgesehen.
</div>

## 💾 Backup-Strategie

Das Homelab ist nicht nur auf Betrieb, sondern auch auf Wiederherstellbarkeit ausgelegt. In der Projektinfo wird klar zwischen System, Daten und aktiven Inhalten getrennt, was ein wichtiges Indiz dafür ist, dass Storage und Recovery nicht als Nebenthema behandelt werden.

<div style="display:flex; gap:20px; align-items:flex-start; flex-wrap:wrap;">
  <div style="flex:1; min-width:280px;">
    <table style="width:100%; border-collapse: collapse;">
      <tr>
        <th align="left">Bereich</th>
        <th align="left">Rolle</th>
      </tr>
      <tr>
        <td>System</td>
        <td>Proxmox / Hypervisor-Basis</td>
      </tr>
      <tr>
        <td>Daten</td>
        <td>HDD-Storage für größere Datenbestände</td>
      </tr>
      <tr>
        <td>Aktive Inhalte</td>
        <td>SSD für Medien, Projekte und laufend genutzte Daten</td>
      </tr>
    </table>
    <p>
      Diese Trennung reduziert Auswirkungen einzelner Fehlerbilder und vereinfacht es, Wiederherstellung und
      Priorisierung im Störfall sauber zu denken.
    </p>
  </div>

  <div style="flex:1; min-width:280px;">
    <!-- FOTO: backup_storage_overview.png - Backup-Ziele, Storage-Aufteilung oder Snapshot-Ansicht -->
    <img src="../assets/backup_storage_overview.png" alt="Storage- und Backup-Aufteilung zwischen System, Daten und aktiven Inhalten">
    <p class="caption">Nachweis folgt</p>
  </div>
</div>

### 🧠 Umsetzung

- Regelmäßige Backups wichtiger Daten und VMs
- Snapshots von VMs innerhalb von Proxmox
- Backup auf separaten Storage innerhalb des Systems
- Perspektivisch Möglichkeit zur externen Sicherung über zweiten Standort

```text
Recovery-Ziel

1. Fehler erkennen
2. VM / Datenstand identifizieren
3. Snapshot oder Backup wiederherstellen
4. Betrieb schnellstmöglich fortsetzen
```

<hr style="border: none; height: 2px; background: linear-gradient(to right, transparent, #ffff, transparent); margin: 30px 0;">

## 🎯 Schutzziele

<table style="width:100%; border-collapse: collapse;">
  <tr>
    <td width="58%" valign="top">
      <ul>
        <li><strong>Schnelle Wiederherstellung:</strong> VMs und wichtige Daten sollen im Fehlerfall zügig zurückgeholt werden können.</li>
        <li><strong>Schutz vor Hardware-Ausfällen:</strong> Die Trennung der Storage-Rollen und der redundante Pool reduzieren Einzelrisiken.</li>
        <li><strong>Grundlage für Offsite-Backups:</strong> Der zweite Standort eröffnet eine sinnvolle Perspektive für externe Sicherungen.</li>
      </ul>
    </td>
    <td width="42%" valign="top">
      <!-- FOTO: proxmox_snapshot_view.png - Snapshot-Ansicht oder Backup-Job im Hypervisor -->
      <img src="../assets/proxmox_snapshot_view.png" alt="Snapshots und Backup-Ansichten innerhalb der Proxmox-Umgebung">
      <p class="caption">Nachweis folgt</p>
    </td>
  </tr>
</table>

<hr style="border: none; height: 2px; background: linear-gradient(to right, transparent, #ffff, transparent); margin: 30px 0;">

## 📊 Monitoring-Status

<div style="display:flex; gap:20px; align-items:flex-start; flex-wrap:wrap;">
  <div style="flex:1; min-width:280px;">
    <p>
      Aktuell ist laut Projektinfo <strong>kein aktives Monitoring</strong> eingerichtet. Das ist fachlich kein
      Makel, solange es offen dokumentiert wird, sondern markiert sauber den Übergang von funktionierendem Betrieb
      zu belastbarer Betriebsbeobachtung.
    </p>
    <div style="background-color: #5c4700; border-left: 6px solid #d4a017; padding: 14px 18px; border-radius: 8px; color: #f8e7a1;">
      <strong>⚠️ In Arbeit:</strong><br>
      Monitoring ist als klares Ausbauthema definiert, aber noch nicht produktiv umgesetzt.
    </div>
    <p><strong>Geplant:</strong></p>
    <ul>
      <li>Systemüberwachung für CPU, RAM und Storage</li>
      <li>Netzwerk-Monitoring</li>
      <li>Alerting bei Problemen</li>
    </ul>
  </div>
  <div style="flex:1; min-width:280px;">
    <!-- FOTO: monitoring_placeholder.png - zukünftiges Monitoring-Dashboard oder Statusansicht -->
    <img src="../assets/monitoring_placeholder.png" alt="Platzhalter für zukünftiges Monitoring-Dashboard des Homelabs">
    <p class="caption">Nachweis folgt</p>
  </div>
</div>

<hr style="border: none; height: 2px; background: linear-gradient(to right, transparent, #ffff, transparent); margin: 30px 0;">

## 🚀 Roadmap

### 🔮 Kurzfristige Ziele

<table style="width:100%; border-collapse: collapse;">
  <tr>
    <th align="left">Vorhaben</th>
    <th align="left">Nutzen</th>
    <th align="left">Status</th>
  </tr>
  <tr>
    <td>VLAN-Segmentierung einführen</td>
    <td>Saubere Netztrennung und bessere Sicherheitszonen</td>
    <td>🔧 Geplant</td>
  </tr>
  <tr>
    <td>Monitoring-System aufsetzen</td>
    <td>Transparenz über Ressourcen und Fehlerzustände</td>
    <td>🔧 Geplant</td>
  </tr>
  <tr>
    <td>Services erweitern</td>
    <td>Breiteres Hosting und realistischere Betriebsfälle</td>
    <td>🔧 Geplant</td>
  </tr>
</table>

### 🌍 Langfristige Ziele

- Eigene Cloud vollständig ausbauen
- Eigene Software 24/7 betreiben
- Automatisierungssysteme entwickeln
- Skalierbare Infrastruktur aufbauen

<hr style="border: none; height: 2px; background: linear-gradient(to right, transparent, #ffff, transparent); margin: 30px 0;">

## 🧠 Lernziele & Projektwert

<table style="width:100%; border-collapse: collapse;">
  <tr>
    <td width="58%" valign="top">
      <ul>
        <li>Netzwerkarchitektur praktisch verstehen</li>
        <li>Virtualisierung im echten Betrieb anwenden</li>
        <li>Infrastruktur selbst aufbauen und verwalten</li>
        <li>DevOps- und Backend-nahe Systeme betreiben</li>
      </ul>
      <p>
        Genau diese Lernziele machen das Projekt später auch für Bewerbungen interessant: Es zeigt nicht nur
        Interesse an Infrastruktur, sondern fortlaufende praktische Arbeit an Betrieb, Erweiterbarkeit und
        technischer Eigenverantwortung.
      </p>
    </td>
    <td width="42%" valign="top">
      <!-- FOTO: homelab_overview_final.png - Gesamtüberblick des Homelabs oder finale Architekturvisualisierung -->
      <img src="../assets/homelab_overview_final.png" alt="Gesamtüberblick der Homelab-Infrastruktur als abschließender Projektnachweis">
      <p class="caption">Nachweis folgt</p>
    </td>
  </tr>
</table>

<hr style="border: none; height: 2px; background: linear-gradient(to right, transparent, #ffff, transparent); margin: 30px 0;">

<div style="background-color: #234; padding: 15px; border-left: 5px solid #38C6FF; border-radius: 5px;">
<strong>📊 FAZIT:</strong><br>
Das Homelab ist bereits so weit entwickelt, dass Themen wie Storage-Trennung, Backup, Standortkopplung und
virtueller Servicebetrieb praktisch bearbeitet werden. Noch offen sind vor allem die klassischen Reifegrade
der nächsten Stufe: Monitoring, detailliertere Segmentierung und der weitere Ausbau hin zu einer noch stärker
automatisierten, skalierbaren Betriebsplattform.
</div>

<hr style="border: none; height: 2px; background: linear-gradient(to right, transparent, #ffff, transparent); margin: 30px 0;">

<p align="center">
  <a href="./03-virtualisierung-dienste.md">Zurück: 03 Virtualisierung & Dienste</a> ·
  <a href="./01-infrastruktur.md">Zurück zum Anfang</a>
</p>
