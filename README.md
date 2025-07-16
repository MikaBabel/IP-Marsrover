Stuktur
Tobias
## 1. Startup des Rovers
   Hotspot <br>
   ### Tastenbelegung
   | Ort an Controller       | Funktion     |
   |:-------------|:-------------:|
   | Joycon links (links rechts) |  Drehen links oder rechts |
   |  Joycon links (oben unten) | Fahren vor und zurück |
   |  Joycon rechts (links rechts) | Im Kreis rotieren (eingeschränkt) |
   |A|Fahren aktivieren (dauerhaft drücken)|
   |B|Turbo Button(deutlich schneller) Vorsicht!|
  


3. Was haben wir geschafft
  - Pi Aufsetzen
      - welche Schritte beendet
      - Wie ist Konfig -> Addressen, Ausrichtung der Servos
         - ### Servos
           Es gibt vier Servos, jeder Servo ist für einen Roboterarm zuständig.<br>
           Die Servos werden über ihren jeweiligen Channel mit dem Mainboard verbunden.<br>
           Damit die Ausrichtung der Roboterarme zum Start gerade ist, wurden explizit Werte gesetzt.<br>
           Die folgenden Tabelle, zeigt die Zuordnung von Servo Position zu Channel zu Ausrichtung des Servos.
           | Ort/Position      | Channel     | Ausrichtung |
           |:-------------|:-------------:|:-------------:|
           | Vorne rechts     | Channel 1    | 141 |
           | Vorne links     |	Channel 2    | 149 |
           | Hinten rechts    | Channel 0    | 139 |
           | Hinten links    | Channel 3    | 138 |
              
           -> Steht auch auf der Platine

        - ### Roboclaws
          Es gibt 3 Roboclaws, jeder Roboclaw ist für 2 Motoren zuständig.<br>
          Die Roboclaws steuern die Motoren an.<br>
          Damit der Pi weiß welchen Roboclaw er über welche Seriennumer (siehe Tabelle) ansteuren kann, müssen diese mit dem Programm BasicMotion konfiguriert werden.
          Hierbei kann man auch die Richtung der Motoren einstellen, z.B. falls sich ein Motor in die falsche Richtung dreht, kann dieser invertiert werden.
          #### Motoren
          <br><img width="379" height="340" alt="Bildschirmfoto 2025-07-16 um 09 56 36" src="https://github.com/user-attachments/assets/6e95f636-20d0-45ad-aa79-3168ef22981e" />
          #### Roboclaw
          <img width="529" height="354" alt="Bildschirmfoto 2025-07-16 um 09 58 23" src="https://github.com/user-attachments/assets/678c52d8-dc31-4b21-9249-2c44bf203b30" />
          
          | Claw(Position auf Board)     | Ort(Motoren)    | SerialNum |
          |:-------------|:-------------:|:-------------:|
          |  Oberster RoboClaw     | Vorne Links & Mitte Links   | 128 |
          |  Unten Vorne RoboClaw    | Hinten L & Hinten R   | 129 |
          |  Unten Hinten RoboClaw  | Vorne Rechts& Mitte Rechts  | 130 |

    - ### Controller Belegung
      Jeder Button/Axe auf dem Controller kann verwendet werden um eine der oben gennanten Funktionen bei der Tastenbelegung annzunehmen.
      Dies wird in der Datei ... eingestellt.
      
      | Axes     | Ort an Controller  |
      |:-------------|:-------------:|
      | 0 | Joycon links (links rechts) |
      | 1 | Joycon links (oben unten)	|
      | 2 | LT |
      | 3 | Joycon rechts (links rechts) |
      | 4 | Joycon rechts (oben unten)	|
      | 5 | RT |
      | 6 | Joypad (links rechts)	|
      | 7 | Joypad (oben unten)	|
   
      | Button | Ort am Controller |
      |--------|--------------------|
      | 0      | A                  |
      | 1      | B                  |
      | 2      | X                  |
      | 3      | Y                  |
      | 4      | LB                 |
      | 5      | RB                 |
      | 6      | Back               |
      | 7      | Start              |
      | 8      | Xbox-Button        |

   - ### Venv
     Damit Python die richtigen Packages vom Venv nimmt, musste in einigen Dateien das Venv explizit angegeben werden.
     

      
  - Simulation
  - 
3. Probleme
5. Next Steps / deren Aufgaben
