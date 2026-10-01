# Merge-Konflikt Doku

Wir haben die README zu zweit bearbeitet, jeder auf seinem eigenen Branch. Ich auf partner-a, mein Partner auf partner-b.

Wie ist das passiert: beide Branches sind vom gleichen Stand in main gestartet. Wir haben dann gleichzeitig die Einleitung in der README geändert, halt jeder anders. partner-a wurde zuerst in main gemergt, das ging noch glatt. Beim Merge von partner-b hat Git dann gestoppt, weil es nicht wusste welche Version stimmen soll. Klassischer Konflikt in README.md mit den <<<<<<< ======= Markern.

Gelöst haben wir das so: wir haben uns die beiden Zeilen zusammen angeschaut und zu einer zusammengefasst statt eine einfach zu löschen. Danach add und commit, damit war der Merge fertig und beide Änderungen drin.

Befehle die dabei liefen: git checkout -b partner-a / partner-b für die zwei Stände, dann git add und git commit pro Branch, git checkout main und git merge partner-a, danach git merge partner-b wo es geknallt hat. Zum Fixen dann README zusammen angepasst, wieder git add README.md und git commit. Zum Schluss git push und mit git log --graph und git status kontrolliert.
