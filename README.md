
# Nornir Chest from God of War Ragnarök

<img width="800" alt="Whole Project" src="https://github.com/user-attachments/assets/a11c25b0-e23d-434e-84f5-f1ce79681e36" />
<img width="800" alt="Chest Close Up" src="https://github.com/user-attachments/assets/bd3d7342-5fbf-4ec0-8018-887896c02c1a" />
<img width="800" alt="Full LEDs Blue" src="https://github.com/user-attachments/assets/ff05a855-5fed-4f55-a47b-937b581707d2" />

  This is a 3D printable replica model of the Nornir Chest from God of War Ragnarök. My goal is to use a variety of electronics to simulate the way the chest works in the game. In God of War, Nornir Chests are puzzles found throughout the map that use their environments to hide and disguise the activators, or seals. There are 4 types of seals: totem poles, braziers, bells, and viking statues. They each have different activation methods, and each is tied to a different rune on the chest. When a seal is activated, the rune on it flashes and disappears, and the corresponding rune on the chest does the same. I ran into a lot of problems getting the interactive electronics to work reliably, including unstable encoder readings, flickering LEDs, and servos that wouldn't move, so the full puzzle isn't finished yet. For now, I'm submitting the project as a lamp and a print-only replica of the chest due to lack of forge points for funding, and lack of materials that are necessary for the finished project.


## My Original Goals

**Brazier** - I planned to use two 7 pixel WS2812B rings and a reed switch. The parts are printed in gold, black, grey, and blue/transparent PLA. The reed switch was supposed to detect the magnetic Blades of Chaos being inserted into the coals. The LED rings would act as a rune and as embers in the fire. The coals are printed with low infill and fewer walls so light can shine through.

**Totem Pole** -  I planned to use 3 diode LEDs and a rotary encoder. It's printed in PLA wood and blue/transparent PLA. The encoder was meant to track the rotation of the pole. The pole connects to a hollow cylinder with three different runes. As it rotates, three LEDs on the side of the pole would light the correct rune.

**Bell** -  I planned to use 1 diode LED and a piezo disk. It's printed in PLA wood, gold, and blue/transparent PLA. The piezo disk was supposed to detect the vibration when the bell is rung, and a dedicated LED would light the rune.

**The Chest**

The plan was for the chest to use three 7 pixel WS2812B rings and a servo. The servo would turn 90 degrees to lock and unlock the chest, and the LEDs would light the runes. The chest is hinged. It's printed in multiple parts to avoid changes between the gold, black, grey, and blue/transparent PLA. Any parts that would otherwise be glued are connected with pins.

**The Base**

The rocky base is a 3d printed shell for the chest chest's electronics. I made room for a breadboard for beginners (like me lol), an Arduino Nano, and a battery pack. All wires go through holes, and the holes have some supports in them when you pull them out. I suggest using a paper clip to push all of the supports out. It shouldn't be too hard.

**Planned Components** 

- Arduino Nano (powered via USB-C)
- 4× WS2812B LED rings (7 LEDs each) – one in each chest rune slot, and 2 in brazier
- 2× Servos – lock the lid
- Rotary encoder – rotating totem
- Reed switch – brazier (detects magnetic Blades of Chaos)
- Piezo disk – tracks bell vibration
- 3× single LEDs – illuminate the runes on the totem
- 1× single LED – illuminates the rune on the bell
- 4× AA battery pack – powers all LEDs and servos

## The Finished Project

The interactive electronics never worked reliably, so I didn't finish the full puzzle. The final project is a lamp and a print-only replica of the chest. Here's how each part ended up.

**Brazier** - The brazier is printed in gold, black, grey, and blue/transparent PLA. The coals are printed with low infill and fewer walls so light can shine through. I planned to use two 7 pixel WS2812B rings and a reed switch to detect the magnetic Blades of Chaos, but I accidentally broke the second LED while soldering, so I ended up only using the LED for the rune. After connecting all LEDs, it flickered like the rest when turned on, but for a short period it worked as intended. The reed switch actually did work great, and still works, which made the brazier the most reliable seal.

**Totem Pole** - The totem pole is printed in PLA wood and blue/transparent PLA. The pole connects to a hollow cylinder with three different runes. I planned to track the rotation with a rotary encoder and light each rune with three LEDs. The encoder readings worked originally, but after using it for a few days the readings started being unstable, with an offset and detents that didn't match. I eventually gave up on the rotary encoder, but it worked for a little bit.

**Bell** - The bell is printed in PLA wood, gold, and blue/transparent PLA. I planned to have a piezo disk detect vibration when the bell is rung and light the rune with a dedicated LED. The piezo sensing actually did end up working fine, but after breaking the first one when putting in the led, I had to replace it with another piezo disk from the bag. It's vibration detection was not accurate, and it for some reason gave me negative readings often. I ended up switching the piezo disk 2 times, but they all gave weird readings after the first one.
The Chest

**The Chest** The chest is hinged. It's printed in multiple parts to avoid changes between the gold, black, grey, and blue/transparent PLA. Any parts that would otherwise be glued are connected with pins. I planned three 7 pixel WS2812B rings and a servo to light the runes and lock the lid. The LEDs flickered or failed and the servo wouldn't move, so the final chest is a lamp and a print-only replica.

**The Base** The rocky base is ended up functioning the same as I planned.

**Printing** The chest uses 5 filaments, mostly Sunlu and Bambu Labs. I printed some parts with a 0.2 mm nozzle, such as the hinges, viking head, and runes, to preserve small details and improve accuracy. I also changed the speed and infill on some parts. For example, the runes are printed in 100% infill grey so light only comes through the rune hole and isn't visible through the plastic. I always used glue, and I used a cheap smooth PEI plate I found on Amazon.

## What Didn't Work

Rotary encoder: unstable readings.

LEDs: flickering and failures.

Servos: wouldn't move.

Piezo disk: unreliable sensing.

Arduino Nano: connection failure.

## Credits

- [Blades of Chaos fridge magnet](https://makerworld.com/en/models/3068479-blades-of-chaos-fridge-magnet#profileId-3454054) — Used as the magnetic Blades of Chaos inserted into the brazier. It is meant to be a fridge magnet.
- [Stone formation base](https://makerworld.com/en/models/2541501-stoneformation-15?from=search#profileId-2798135) — This is the rocky base I used. I modified it to have a central port for all the electronics and indents to connect the chest and three seals.
- [HW-040 module case housing enclosure](https://makerworld.com/en/models/1896813-hw-040-module-case-housing-enclosure?from=search#profileId-2032305) — This is the enclosure I used for the rotary encoder.
- [Print-in-PLAce hinge set](https://makerworld.com/en/models/791901-print-in-PLAce-hinge-set?from=search#profileId-730453) — This is the hinge I used. I modified it to have extruded pins and be much smaller.

## Updates

- Added a fully 3D-printable version.
- Will update firmware to fit physical chest wherever needed.

## Get .blend File Here
(I'm also a noob to github lol. I can't figure out how to upload large files.)

https://drive.google.com/file/d/1p0lWug-2twfeMgqFWuvS9LOxBlz-mlpI/view?usp=sharing


## Updated BOM

<img width="1066" height="472" alt="Screenshot 2026-08-14 at 5 10 53 PM" src="https://github.com/user-attachments/assets/daeb57f7-734c-46ce-97fb-86468f2cc218" />



