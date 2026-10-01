# Firewall Grundlagen

Firewall ist im Grunde der Türsteher im Netz. Die schaut, was rein und raus darf, und blockt den Rest. Ohne das Teil steht halt alles offen.

Es gibt zwei Arten. Paketfilter schauen sich IP, Port und Protokoll an und entscheiden nach Regeln. Stateful prüft zusätzlich, ob das Paket zu einer bestehenden Verbindung gehört, das ist schon deutlich schlauer.

Wichtig sind die Richtungen. Inbound ist was von außen reinkommt, Outbound was von innen rausgeht. Standard ist eigentlich alles verbieten und nur das nötigste erlauben. Andersrum wirds schnell löchrig.

In der Praxis heißt das: nur Ports aufmachen die man braucht, also z.B. 443 für Web, 22 für SSH wenn nötig. Rest zu. Dazu noch Logging an, damit man sieht wenn was geblockt wird und ob da ständig einer gegen die Wand rennt.

Bei uns läuft das auf dem Router plus Windows Firewall auf den Servern. Doppelt hält besser, und man sollte die Regeln ab und zu aufräumen, sonst sammelt sich da Mist an den keiner mehr versteht.
