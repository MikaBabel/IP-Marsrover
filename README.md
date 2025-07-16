## Startup Rovers
Zum Starten und Fahren des Rovers sind die folgenden Schritte notwendig
### Hotspot Erstellen
Um den Respberry Pi des Rovers über SSH anzusteuern, muss ein Hotspot mit den folgenden Daten erstellt werden:

      SSID/Name: MarsNet
      Passwort: MarsRover
  - Während unserer Arbeit hat es sich als satbiler erwiesen, den **Hotspot über ein seperates Samrtphone** statt den Cleint Rechner zu öffnen.   
  - Um die **IP Addresse des Pis** für die erste SSH Verbindung zu erhalten, kann dies jedoch ein **Hotspot über Windows** liefern.

### Powerup Rover
1. Akku Einlegen und Anschließen
2. Schalter an der Rückseite des Rovers nach oben Umlegen.
      - Das Display auf der Rckseite sollte aufleuchten und **mindestens ~11V** anzeigen.
      - Die LEDS des Brainboads sollten nun auch die 5V bestätigen.
      - Falls der die Voltzahl darunter liegt, den Akku laden. link zum richtig laden einfügen
            
### Controller an den Pi Anschließen
Als nächstes wird ein Controller über die USB Schnittstellen des Pis angeschlossen.   
Bisher wurde dafür ein **XBox 360 Controller** dafür verwendet.      
- Soll ein anderer Controller verwedet werden und unerwartet die Bewegung nicht mehr wie beschrieben funktionieren, kann das Buttonmapping angepasst werden.
      

### SSH Verbindung zum Rover
Nachdem sich der PI mit dem Hotspot verbunden hat und im Netz sichtbar ist, werden folgede Schritte ausgeführt:
- Der Pi kann dabei bis zu 5 min brauchen bis er vollständig erreichbar ist.
      
#### 1. Mit bekannter IP Addresse
Falls die IP Addresse des PIs bekannt ist, zb durch Auslesen über den Windows Hotspot, erfolgt die erste Verbindung wie folgt:
 
      ssh rover@IP-des-Pis
      Passwort: mars
#### 2. Über MacOs, mittels .local
Falls die IP noch nicht bekannt ist, unterstüzt MacOS Bonjour:

      ssh rover@marsrover.local
      Passwort: mars
#### 3. Nach erfolgreicher Anmeldung
Nach erfolgreicher Erstanmeldung dann über:
   
      ssh rover@marsrover
      Passwort: mars


5. Was haben wir geschafft
  - Pi Aufsetzen
     - Betriebssystem: Ubutnu
      - welche Schritte beendet
      - Wie ist Konfig -> Addressen, Ausrichtung der Servos
        
  - Simulation
  - Akkus richtig laden-> Anleitung
3. Probleme
Checken des wiring: https://github.com/nasa-jpl/open-source-rover/blob/master/electrical/pcb/README.md
5. Next Steps / deren Aufgaben
