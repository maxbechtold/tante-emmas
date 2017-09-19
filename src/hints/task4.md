Definition von Input Abhängigkeiten (10 min)
============================================
* Der Grund für die fehlschlagenden Tests ist eine nicht definierte Quelle von Input
    * Input sind Zustände die den Programmfluss beeinflussen, die aber nicht unmittelbar vom Programm (sondern von externen Quellen) gesteuert werden
    * Beispiele: Ergebnisse von Webservice-Aufrufen, Dateizugriff, Zufallszahlen, Zeitanfragen
* Findet die Input Methode(n) und annotiert sie mit `@Input` (Input kann in Form von Rückgabewerten oder Seiteneffekten auf Argumenten erfolgen, testrecorder beherrscht beides)
* Der Aufruf der Input-Methode muss von `AgentConfig.getPackages` abgedeckt werden
* Startet das Launchscript
* Verwendet die Anwendung und generiert ein paar Tests
* Stoppt den Server und untersucht die Tests
* Alles enspannt? Die Tests sollten laufen