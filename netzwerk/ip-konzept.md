# IP-Konzept (IPv4 Grundlagen)

## 1. Grundlagen der IPv4-Adressierung
Eine IPv4-Adresse ist 32 Bit lang und wird in 4 Oktetten zu je 8 Bit dargestellt (z. B. `192.168.1.10`).
Der Adressraum umfasst ca. 4,3 Milliarden Adressen.

## 2. Aufbau: Netzwerk- und Hostanteil
Jede IP-Adresse besteht aus einem Netzwerkanteil und einem Hostanteil.
Die Subnetzmaske (z. B. `255.255.255.0` bzw. `/24`) legt fest, welcher Teil zum Netzwerk gehört.
Alle Hosts im gleichen Netz teilen sich den Netzwerkanteil.

## 3. Private und öffentliche Adressen
Private Bereiche (RFC 1918): `10.0.0.0/8`, `172.16.0.0/12`, `192.168.0.0/16`.
Private Adressen werden nur intern geroutet und per NAT ins Internet übersetzt.

## 4. Sonderadressen
- `127.0.0.1`: Loopback (localhost)
- `0.0.0.0/0`: Standardroute
- `255.255.255.255`: Broadcast
- APIPA `169.254.0.0/16`: automatische Adresse bei fehlendem DHCP

## 5. Subnetting-Beispiel
Netz `192.168.1.0/24`: 254 nutzbare Hosts (`192.168.1.1` bis `192.168.1.254`).
Netz-ID: `192.168.1.0`, Broadcast: `192.168.1.255`.
Gateway (z. B. `.1`) und DNS müssen auf Clients korrekt konfiguriert sein (statisch oder per DHCP).
