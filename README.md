# home-assistant-kleinspeicher-pv-automation
Dieser Blueprint steuert einen 5-Liter-Durchlauferhitzer (!!Druckfest!!) („Kleinspeicher“) zur effizienten Nutzung von PV-Stromüberschuss. Der Kleinspeicher ist hydraulisch am Kaltwasserzulauf des Hauptwarmwasserspeichers angeschlossen und pumpt bei ausreichend PV-Energie erwärmtes Wasser über ein Strangregulierventil in den Zirkulationseingang zurück in den Speicher.
Das Strangregulierventil dient dazu nur eine bestimmte menge Wasser durchzulassen damit der Kleinspeicher genug zeit hat das Wasser zu erwährmen. Ich habe mein Strangregulierventil auf 28 Liter pro Minute eingestellt.
Den oberen Temperatur Wert zur Abschaltung am besten auf 69 Grad Celsius stehen lassen da ab dieser Temperatur keine effiziente Erwährmung mehr Stattfindet und der Kleinspeicher viel ein und aus taktet.
Die Automation schaltet den Kleinspeicher ein, wenn die Netz Einspeisung aus der PV- Anlage einen konfigurierbaren Schwellenwert überschreitet (bitte Mindest 200 Watt Puffer lassen) und der Warmwasserspeicher unter einer bestimmten Temperatur liegt. Die Pumpe wird dabei mit zeitlicher Verzögerung aktiviert, um eine Vorwärmung sicherzustellen.
Wird die gewünschte Temperatur erreicht oder fällt die Einspeisung dauerhaft unter einen Mindestwert, schaltet die Steuerung den Kleinspeicher automatisch wieder ab. So wird überschüssige Sonnenenergie gezielt zur Warmwasser- unterstützung genutzt, ohne Netzstrom zu verbrauchen.

Es ist zu empfehlen das Gerät von einem Fachmann Installieren und anschließen zu lassen.

Um den Bleprint in HA einzufügen gehe zu Einstellungen -> Automationen und Szenen -> Blueprints 
und klicke dann auf "Blueprint importieren" und füge diesen Link ein: https://github.com/JojoLP7306/home-assistant-kleinspeicher-pv-automation/blob/main/blueprint.yaml
