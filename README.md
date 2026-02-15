# Cornflakes Machine - Coolest Projects 🥣
Dit project is een automatische cornflakes dispenser, ontworpen en gebouwd door **Oliver** voor **Coolest Projects 2026**. 
Het combineert lasersnijwerk, 3D-geprinte onderdelen en elektronica aangestuurd door een Micro:bit.

## 📁 Projectstructuur
Hieronder vind je een overzicht van hoe de bestanden in dit project zijn georganiseerd:

```text
cornflakes-dispenser/
├── code/
│   └── microbit-cornflakes.hex     			# De kant-en-klare code voor de Micro:bit
├── modellen/
│   ├── 3d-print/                   			# Onderdelen voor de 3D-printer
│   │   ├── cilinder cornflakes machiene.stl  	# Het draaimechanisme
│   │   ├── pi handvat.stl                    	# Handvat voor bediening
│   │   ├── sensor houder.stl                 	# Bevestiging voor de afstandssensor
│   │   └── servo houder 2.0.stl              	# Stevige houder voor de servo motor
│   └── lasercut/                   			# Bestanden voor de lasersnijder (SVG)
│       ├── binnen box.svg                    	# Het interne mechanisme frame
│       └── buiten box.svg                    	# De behuizing van de machine
└── README.md                       			# Deze handleiding
```

## 🛠 Hardware Onderdelen
- **Controller:** Micro:bit (v2)
- **Actuator:** Servo motor sg90(voor het doseermechanisme)
- **Sensoren:** 
  - Afstandssensor HC-SR04(om een kom te detecteren)
  - Drukknop (voor handmatige bediening)
- **Output:** LED's van 5mm met houder van 5mm (voor status)

## 🔧 Montage instructies

### 1. Behuizing (Lasercutter)
Gebruik de bestanden in `modellen/lasercut/`. 
- **Buiten box:** De hoofdomgeving van de dispenser.
- **Binnen box:** Voor de montage van alle interne onderdelen.
- *Materiaaladvies:* 4mm multiplex.

### 2. Mechanisme (3D-printer en Lasercutter)
Print de onderdelen in `modellen/3d-print/`. De `cilinder` is het belangrijkste onderdeel dat de cornflakes verplaatst. De `servo houder` zorgt dat de motor precies op de juiste plek blijft zitten.
De Lasercutter en 3D-printer kunt u gebruiken in een FabLab ergens in België.

### 3. Elektronica & Software
1. upload het bestand `code/microbit-cornflakes.hex` naar je Micro:bit.
2. Sluit de servo aan op de Micro:bit (Pin 2).
3. Bevestig de sensor in de `sensor houder` en sluit deze aan op Pin 1.
4. Sluit rode led aan met een weerstand op pin 8
5. Sluit blauwe led aan met een weerstand op pin 5 
6. Sluit groene led aan met een weerstand op pin 6
7. Sluit oranje led aan met een weerstand op pin 7
8. Sluit knop aan op pin 0
9. Voor de ledjes kun je ook andere pinnen gebruiken als je dat wilt.

## 💻 Hoe het werkt
De machine wacht tot er een kom voor de sensor wordt geplaatst. Zodra de sensor een afstand meet die kleiner is dan de drempelwaarde, dan moet jij op de drukknop drukken om de servo te activeren. De cilinder draait dan een kwartslag om cornflakes te lossen en draait daarna weer terug.
Als er een kom voor de sensor staat dan gaat er een groen ledje branden en kan je op de knop drukken om de cornflakes te verdelen. Waneer het machien bezig is knippert er een oranje led.
Als er niets voor de sensor staat en je drukt op de knop gaat er een rood ledje aan. Als het machien gewoon aanstaat dan brand er een blauw ledje.

## 🏆 Over de maker
Gemaakt door Oliver voor de Coolest Projects competitie. Veel plezier met bouwen!
