# Merge-Konflikt Doku

Hab das mit zwei Branches nachgestellt, weil kein zweiter Rechner da war. Also im Grunde Zusammenarbeit simuliert.

Wie ist das passiert: beide Branches sind vom gleichen Stand gestartet. partner-a und partner-b haben dann die gleiche Zeile in der README geändert, halt jeder anders. partner-a zuerst in main gemergt, das ging noch glatt. Beim zweiten Merge mit partner-b hat Git dann gemeckert, weil es nicht wusste welche Version stimmen soll. Klassischer Konflikt in README.md mit den <<<<<<< ======= Markern.

Gelöst hab ichs so: Datei aufgemacht, beide Zeilen angeschaut und zu einer zusammengefasst statt eine einfach zu löschen. Danach add und commit, damit war der Merge fertig.

Befehle die dabei liefen: git checkout -b partner-a / partner-b für die zwei Stände, dann git add und git commit pro Branch, git checkout main und git merge partner-a, danach git merge partner-b wo es geknallt hat. Zum Fixen dann README von Hand angepasst, wieder git add README.md und git commit. Zum Schluss git push und mit git log --graph und git status kontrolliert.
