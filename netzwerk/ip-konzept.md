# IP-Konzept IPv4

IPv4 ist im Grunde immer noch das, womit man täglich zu tun hat. Eine Adresse hat 32 Bit, also vier Blöcke wie 192.168.1.10. Reicht rechnerisch für ca. 4,3 Milliarden Adressen, was halt längst zu wenig ist, aber läuft trotzdem überall.

Aufgebaut ist das immer gleich, vorne Netzanteil, hinten Hostanteil. Die Subnetzmaske sagt dir, wo getrennt wird. Klassiker ist 255.255.255.0, also /24. Heißt alle mit gleichem Netzanteil sind im selben Netz.

Dann gibts privat und öffentlich. Privat ist 10.0.0.0/8, 172.16.0.0/12 und 192.168.0.0/16. Die nimmst du intern, raus gehts dann über NAT. Öffentliche kriegst du vom Provider.

Paar Sonderfälle muss man kennen. 127.0.0.1 ist localhost, 255.255.255.255 Broadcast, und 169.254.x.x kriegst du automatisch wenn kein DHCP antwortet. Da stimmt dann meist was nicht.

Beispiel aus der Praxis: 192.168.1.0/24. Netz-ID ist .0, Broadcast .255. Nutzen kannst du .1 bis .254, also 254 Hosts. Gateway liegt meist auf der .1, DNS und IP kommen per DHCP oder du trägst sie von Hand ein.
