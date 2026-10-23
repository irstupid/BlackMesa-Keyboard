# Keyboard Project

the first week of hack clubs half life thing.

i have a friend who asked me to make a keyboard for him and i was like "oh sure that sounds fun" and now i am finaly getting around to it

- it runs on a raspberry pi pico using QMK as its main firmware (more details in the firmware section once i do that)
- it is TKL
- it has 90 neopixle addressable LEDS
- it has a custom case (also unfinished, will update once done)

## Schematic
<img width="757" height="690" alt="KeyboardSchematic4" src="https://github.com/user-attachments/assets/4605cac1-a2ba-4e26-9103-0efb8c7bd926" />

also here is the row/column layout if you were wondering

<img width="1006" height="503" alt="KeyboardMap" src="https://github.com/user-attachments/assets/2f57a470-374a-498b-a8e4-d9d328fb1046" />

## PCB
<img width="948" height="350" alt="Keyboard3DFront" src="https://github.com/user-attachments/assets/a447795d-d434-4a85-a984-5c35deb25001" />
<img width="1422" height="524" alt="KeyboardLayout3" src="https://github.com/user-attachments/assets/84a7980f-8b5d-44f0-9a47-f2c5b279af08" />
i was initially going to add a silkscreen but ran out of inspiration and time. i might still do that it have have any ideas.
the BOM only has the board and none of the parts because i am sourcing those externally.
the usbc on the pico pointing inward is intentional, the cable will go along the bottom and through the back side of the case.

## Firmware
it will use QMK for the keyboard and some custom program for controlling the LEDS on a separate core.
i will work on the firmware once i have a pico and board to test on

## Case
the case will be made from a 3d printed part and a sanded acrylic key plate. here is a rough sketch

<img width="401" height="281" alt="KeyboardSideView" src="https://github.com/user-attachments/assets/da044e0b-f85e-4bc2-a250-d01e0f6e88d0" />

everything will be machined in house at my school. i will add more details once done

.

.

.

.

i was initially skeptical of markdowns but i actually really like how they handle formatting, i might start using them more. hopefully this readme is ok!
