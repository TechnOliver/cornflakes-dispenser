# Cornflakes Machine - Coolest Projects 🥣
Dit project is een automatische cornflakes dispenser, ontworpen en gebouwd door **Oliver** voor **Coolest Projects**. Het combineert lasersnijwerk, 3D-geprinte onderdelen en elektronica aangestuurd door een Micro:bit.

## 📁 Projectstructuur
Hieronder vind je een overzicht van hoe de bestanden in dit project zijn georganiseerd:

```text
cornflakes-dispenser/
├── code/
│   └── microbit-cornflakes.hex     # De kant-en-klare code voor de Micro:bit
├── modellen/
│   ├── 3d-print/                   # Onderdelen voor de 3D-printer
│   │   ├── cilinder cornflakes machiene.stl  # Het draaimechanisme
│   │   ├── pi handvat.stl                    # Handvat voor bediening
│   │   ├── sensor houder.stl                 # Bevestiging voor de afstandssensor
│   │   └── servo houder 2.0.stl              # Stevige houder voor de servo motor
│   └── lasercut/                   # Bestanden voor de lasersnijder (SVG)
│       ├── binnen box.svg                    # Het interne mechanisme frame
│       └── buiten box.svg                    # De behuizing van de machine
└── README.md                       # Deze handleiding
```

## 🛠 Hardware Onderdelen
- **Controller:** Micro:bit (v1 of v2)
- **Actuator:** Servo motor (voor het doseermechanisme)
- **Sensoren:** 
  - Afstandssensor (om een kom te detecteren)
  - Drukknoppen (voor handmatige bediening)
- **Output:** LED's (voor verlichting en status)

## 🔧 Montage instructies

### 1. Behuizing (Lasercutter)
Gebruik de bestanden in `modellen/lasercut/`. 
- **Buiten box:** De hoofdomgeving van de dispenser.
- **Binnen box:** Zorgt voor de geleiding van de cornflakes naar het draaimechanisme.
- *Materiaaladvies:* 3mm of 4mm multiplex.

### 2. Mechanisme (3D-printer)
Print de onderdelen in `modellen/3d-print/`. De `cilinder` is het belangrijkste onderdeel dat de cornflakes verplaatst. De `servo houder` zorgt dat de motor precies op de juiste plek blijft zitten.

### 3. Elektronica & Software
1. Flash het bestand `code/microbit-cornflakes.hex` naar je Micro:bit.
2. Sluit de servo aan op de Micro:bit (Pin 0).
3. Bevestig de sensor in de `sensor houder` en sluit deze aan op Pin 1.

## 💻 Hoe het werkt
De machine wacht tot er een kom voor de sensor wordt geplaatst. Zodra de sensor een afstand meet die kleiner is dan de drempelwaarde, zal de Micro:bit de servo aansturen. De cilinder draait dan een kwartslag om cornflakes te lossen en draait daarna weer terug.

## 🏆 Over de maker
Gemaakt door Oliver voor de Coolest Projects competitie. Veel plezier met bouwen!
