Beheben von Fehlern (15 min)
============================
* Vermutlich hat der eine oder andere schon Fehler im Code gefunden
    * Der Kunde hat das Gefühl dass die Preise nach einem Regentag dauerhaft höher sind ...
    * Ein Tester meinte das manche Aktionen dazu führen, dass sich alle Produkte in Zukunft preislich anders verhalten
* Findet die Variable in der die Produkte abgebildet werden
* Findet die Änderung an dem Produkt die vermutlich nicht beabsichtigt war
* Findet Tests, die die unbeabsichtigte Änderung fixieren
* Wir gehen nun testgetrieben vor:
    * korrigiert die Tests in der Art und Weise, dass sie das wirklich erwartete Verhalten reflektieren
    * korrigiert den Code
* Startet die Tests erneut
    * Vielleicht habt ihr Tests übersehen, wenn sie ebenfalls eine unbeabsichtigen Änderung spezifizieren -> korrigiert sie
    * Es gibt vielleicht auch andere Tests, die jetzt fehlschlagen -> Diskutiert wie hier eine Lösung aussehen könnte
    * Im Zweifelsfall (und wenn man sicher ist, dass die eigene Implementierung korrekt ist) kann man natürlich auch einfach neue Tests generieren

* Feedback im Anschluss oder hier:
<img src="qrcode.png" width="400px"/>