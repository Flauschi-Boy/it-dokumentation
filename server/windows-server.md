# Windows Server – Rollen und Features

## 1. Was sind Rollen?
Rollen erweitern einen Windows Server um zentrale Netzwerkdienste (z. B. AD DS, DNS, DHCP).
Sie werden über den Server-Manager oder PowerShell (`Install-WindowsFeature`) installiert.
Pro Server sollten nur benötigte Rollen installiert werden (Sicherheit, Performance).

## 2. Wichtige Rollen im Überblick
- **AD DS (Active Directory Domain Services):** zentrale Benutzer-, Gruppen- und Computerverwaltung, Kerberos-Authentifizierung.
- **DNS:** Namensauflösung (Hostname zu IP), Voraussetzung für AD DS.
- **DHCP:** automatische Vergabe von IP-Adressen, Gateway und DNS an Clients.
- **Datei- und Speicherdienste:** Freigaben (SMB), NTFS-Berechtigungen, Kontingente.
- **Webserver (IIS):** Hosting von Webseiten und Webanwendungen.
- **Hyper-V:** Virtualisierung von Gastsystemen auf dem Host.
- **Print Services:** zentraler Druckserver mit Treiberverteilung.

## 3. Best Practices
Rollen nach Funktion auf Server verteilen (z. B. DC + DNS/DHCP getrennt von Fileserver).
Regelmäßig Updates einspielen und nur benötigte Firewall-Ports freigeben.
Änderungen und Konfigurationen in dieser Dokumentation festhalten.
