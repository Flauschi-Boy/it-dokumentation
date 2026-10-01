# Windows Server Rollen

Rollen sind beim Windows Server einfach die Dienste, die du nachinstallierst. Geht über den Server-Manager oder schnell per PowerShell. Ehrlich gesagt nur installieren was man wirklich braucht, Rest macht die Kiste nur angreifbar und langsam.

AD DS ist das zentrale Ding für Benutzer, Gruppen und Rechner in der Domäne. Läuft nur sauber mit DNS zusammen, das gehört also fast immer dazu. DHCP verteilt dann IP, Gateway und DNS an die Clients, spart ne Menge Handarbeit.

Dazu kommen noch die Klassiker. Dateidienste für Freigaben per SMB mit NTFS-Rechten, IIS wenn du Webseiten hosten willst, Hyper-V für VMs und Druckdienste wenn du Drucker zentral verwalten willst.

Wir trennen das so gut es geht, also DC mit DNS/DHCP extra und Fileserver extra. Updates rein, Firewall nur das nötigste auf, und Änderungen kurz hier festhalten.
