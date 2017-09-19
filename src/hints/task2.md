Testrecorder Installieren (10 min)
==================================

* Legt testrecorder-0.3.x-jar-with-dependencies.jar in euren Workspace
* Fügt testrecorder-0.3.x-jar-with-dependencies.jar dem Klassenpfad hinzu
* Kopiert `AgentConfig.java` ins Package `net.amygdalum.tanteemmas.testrecorder` im Verzeichnis src/main/java 
* Macht euch mit der Konfiguration in `AgentConfig.java` vertraut
* Modifiziert das Launchscript durch einfügen von  `-javaagent:testrecorder-0.3.x-jar-with-dependencies.jar=net.amygdalum.tanteemmas.testrecorder.AgentConfig`
    * eclipse: run configurations -> TanteEmmas -> Arguments -> Vm Arguments
    * intellij: run -> edit configurations -> tante-emmas -> Vm Options
    * shell: `java -cp [classpath] -javaagent:[...] io.vertx.core.Launcher run net.amygdalum.tanteemmas.server.Server`
* Startet das Launchscript
    * Der Server startet nun mit `loading AgentConfig`
    * Wenn nicht, stattdessen mit `loading default config`? Dann wurde die Klasse `AgentConfig` nicht gefunden (prüft die Packages auf Rechtschreibfehler) 
    * Wenn nicht? Dann wurde der agent nicht geladen (der Pfad zur `testrecorderXXX.jar` ist wohl falsch)
* Stoppt den Server
* Annotiert `PriceCalculator.computePrice` mit `@Recorded`
* Startet das Launchscript
    * es startet mit `loading AgentConfig`
    * es folgt `recording snapshots of ...`
    * andernfalls Konfiguration prüfen
* Navigiert zu http://localhost:8080
* Benutzt die Anwendung
* Beobachtet die Konsole und die dort geloggten Tests
* Stoppt den Server und untersucht die generierten Tests im target-Verzeichnis
* Keine Sorge wenn die Tests noch nicht laufen ... wir beheben das später