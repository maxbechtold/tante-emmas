Globale Abhängigkeiten Eliminieren (10 min)
===========================================
* Der Grund für die fehlschlagenden Tests ist eine Statische Variable, die nicht aufgezeichnet wurde
    * Statische/Globale Variablen müssen explizit konfiguriert werden
* Findet die globale Variable
* Annotiert sie mit `@Global`
* Startet das Launchscript
* Verwendet die Anwendung und generiert ein paar Tests
* Stoppt den Server und untersucht die Tests
* Einige Tests laufen hoffentlich, keine Sorge: Auch um die übrigen Tests kümmern wir uns noch. 