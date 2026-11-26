# Nornir Chest from God of War Ragnarök

<img width="800" alt="Whole Project" src="https://github.com/user-attachments/assets/a11c25b0-e23d-434e-84f5-f1ce79681e36" />
<img width="800" alt="Chest Close Up" src="https://github.com/user-attachments/assets/bd3d7342-5fbf-4ec0-8018-887896c02c1a" />
<img width="800" alt="Full LEDs Blue" src="https://github.com/user-attachments/assets/ff05a855-5fed-4f55-a47b-937b581707d2" />

This is a 3D printable replica model of the Nornir Chest from God of War Ragnarök. My goal was to use a variety of electronics to simulate the way the chest works in the game. In God of War, Nornir Chests are puzzles found throughout the map that use their environments to hide and disguise the activators, or seals. There are 4 types of seals: totem poles, braziers, bells, and viking statues. They each have different activation methods, and each is tied to a different rune on the chest. When a seal is activated, the rune on it flashes and disappears, and the corresponding rune on the chest does the same.

I built and tested the electronics, and each part worked at some point, but I never got them all working reliably together. The servos stopped moving, several LEDs broke, the rotary encoder stopped tracking consistently, the bell sensor became unreliable, and my Nano stopped connecting to my computer. I'm submitting the project as a **lamp version** and a **fully print-only replica**, because I ran out of Forge points for funding and out of working parts. The interactive puzzle version is unfinished.

## My Original Goals

**Brazier** - I planned to use two 7 pixel WS2812B rings and a reed switch. The parts are printed in gold, black, grey, and blue/transparent PLA. The reed switch was supposed to detect the magnetic Blades of Chaos being inserted into the coals. The LED rings would act as a rune and as embers in the fire. The coals are printed with low infill and fewer walls so light can shine through.

**Totem Pole** - I planned to use 3 LEDs and a rotary encoder. It's printed in PLA wood and blue/transparent PLA. The encoder was meant to track the rotation of the pole. The pole connects to a hollow cylinder with three different runes. As it rotates, three LEDs on the side of the pole would light the correct rune.

**Bell** - I planned to use 1 LED and a piezo disk. It's printed in PLA wood, gold, and blue/transparent PLA. The piezo disk was supposed to detect the vibration when the bell is rung, and a dedicated LED would light the rune.

**The Chest** - The plan was for the chest to use three 7 pixel WS2812B rings and two MG90 servos. The servos would turn 90 degrees to lock and unlock the lid, and the LEDs would light the runes. The chest is hinged. It's printed in multiple parts to avoid changes between the gold, black, grey, and blue/transparent PLA. Any parts that would otherwise be glued are connected with pins.

**The Base** - The rocky base is a 3D printed shell for the chest's electronics. I made room for a breadboard for beginners (like me lol), an Arduino Nano, and a battery pack. All wires go through holes, and the holes have some supports in them when you pull them out. I suggest using a paper clip to push all of the supports out. It shouldn't be too hard.

## The Finished Project

Everything is printed and assembled. The electronics were built and tested piece by piece, but they never worked reliably all at once. Here's how each part ended up.

**Brazier** - The brazier is printed in gold, black, grey, and blue/transparent PLA. The coals are printed with low infill and fewer walls so light can shine through. The reed switch worked great from the start and still works. I tested it with an LED, and it detects the magnetic Blades of Chaos fridge magnet. It was the most reliable seal. I planned two LED rings but only ended up using one for the rune. Later, the ground pad on that ring fell off and shorted against 5V, which destroyed it, and I had no replacement.

**Totem Pole** - The totem pole is printed in PLA wood and blue/transparent PLA. The pole connects to a hollow cylinder with three different runes. The diode LEDs I ordered arrived with bad internals, and the LED strip I bought was too hard to solder. I ended up using a piece of LED strip from my school. At first the rotary encoder worked well. The LEDs flashed red for a wrong rune and white for the correct rune. I fixed a bug where the encoder always thought it started on F. To do that, I added EEPROM position saving, a hold-for-3-seconds calibration button, and a reset button. Later the readings became inconsistent. For example, turning F to C counted 19, 15, 22, and then 15 increments. I eventually gave up on it.

**Bell** - The bell is printed in PLA wood, gold, and blue/transparent PLA. The first LEDs I tried kept losing their copper pads, so I used an LED module I found in a bin. It worked until it stopped working later on. The bell and stand were too small for the wires and LED at first, so I resized and reprinted them. I hot glued the parts together so they hold without tape. The piezo disk worked at first. Then I tore a wire pad off it while removing the LED and replaced it. The replacements gave erratic readings, including large negative values, and I had to replace them twice.

**The Chest** - The chest is hinged. It's printed in multiple parts to avoid changes between the gold, black, grey, and blue/transparent PLA. Any parts that would otherwise be glued are connected with pins. The chest LEDs worked well when I first connected them. After I broke three rings while soldering, I got the last one working by resoldering it. They later started to flicker, and that continued even with everything else disconnected. The lid lock went through a redesign, because the first servo arm didn't fit. I replaced the lid slot with an extruded handle that the servo arms block, and it worked. Later the servos only made grinding sounds, and replacing them didn't fix it.

**The Base** - The rocky base ended up working the same as I planned. It's a modified version of a MakerWorld model, and it prints in four pieces because it's too big for my printer bed.

**Printing** - The chest uses 5 filaments, mostly Sunlu and Bambu Labs. I printed some parts with a 0.2 mm nozzle, such as the hinges, viking head, and runes, to preserve small details and improve accuracy. I also changed the speed and infill on some parts. For example, the runes are printed in 100% infill grey so light only comes through the rune hole and isn't visible through the plastic. I always used glue, and I used a cheap smooth PEI plate I found on Amazon.

## What Didn't Work

- Rotary encoder: it worked at first, but the readings became inconsistent.
- LEDs: the chest rings flickered. One ring was destroyed by a short, and others were lost to soldering damage.
- Servos: they worked after the lid redesign, then stopped moving.
- Piezo disk: the replacement disks gave erratic readings.
- Arduino Nano: one burned out and the second stopped connecting to my computer.
- Soldering: pads kept lifting off the LED rings and small LEDs.

## Final Parts List

This is everything I used for the final build, including parts that later broke. Quantities marked ⚠️ are my best guess.

**Electronics**
- Arduino Nano ×2 (the first burned out, and the replacement stopped connecting; pin headers soldered on)
- WS2812B 7-LED rings: 3 in the chest, 1 in the brazier (a second brazier ring was planned and broken during soldering)
- LED strip piece (from school) for the totem pole runes
- LED module (from a bin) for the bell rune
- MG90 servos ×2 (replaced several times)
- HW-040 rotary encoder module
- Reed switch
- Piezo disk ⚠️ (3 used in total)
- Push buttons: one for totem calibration and one for reset ⚠️
- Switch for opening and closing the servos in testing ⚠️
- 4× AA battery holder with switch ⚠️
- Breadboard
- Dupont wires and connectors
- Solder and tape

**Other**
- Blades of Chaos fridge magnet (3D printed)
- Lamp kit from Bambu Lab (lamp version) ⚠️
- Hot glue
- Printing supplies: PLA in gold, black, grey, and blue/transparent, plus PLA wood, a 0.2 mm nozzle, glue, and a smooth PEI plate

## Credits

- [Blades of Chaos fridge magnet](https://makerworld.com/en/models/3068479-blades-of-chaos-fridge-magnet#profileId-3454054) — Used as the magnetic Blades of Chaos inserted into the brazier. It is meant to be a fridge magnet.
- [Stone formation base](https://makerworld.com/en/models/2541501-stoneformation-15?from=search#profileId-2798135) — This is the rocky base I used. I modified it to have a central port for all the electronics and indents to connect the chest and three seals.
- [HW-040 module case housing enclosure](https://makerworld.com/en/models/1896813-hw-040-module-case-housing-enclosure?from=search#profileId-2032305) — This is the enclosure I used for the rotary encoder.
- [Print-in-PLAce hinge set](https://makerworld.com/en/models/791901-print-in-PLAce-hinge-set?from=search#profileId-730453) — This is the hinge I used. I modified it to have extruded pins and be much smaller.

## Updates

- Added a fully 3D-printable version.
- Added a lamp version.
- Firmware will need updating to fit the physical chest if I rebuild the electronics.

## Get .blend File Here
(I'm also a noob to GitHub lol. I can't figure out how to upload large files.)

https://drive.google.com/file/d/1p0lWug-2twfeMgqFWuvS9LOxBlz-mlpI/view?usp=sharing

## Updated BOM

<img width="1066" height="472" alt="Screenshot 2026-08-14 at 5 10 53 PM" src="https://github.com/user-attachments/assets/daeb57f7-734c-46ce-97fb-86468f2cc218" />
