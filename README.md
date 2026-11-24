# Keyboard Project

the first week of hack clubs half life thing.

i have a friend who asked me to make a keyboard for him and i was like "oh sure that sounds fun" and now i am finaly getting around to it

- it runs on a raspberry pi pico using QMK as its main firmware (more details in the firmware section once i do that)
- it is TKL
- it has 90 neopixle addressable LEDS
- it has a custom case (also unfinished, will update once done)

## THE PICO USB
after writing this section i realized i got maybe a little annoyed and crashed out a little, but im keeping it like this because i think its valid to get a little annoyed that my project has been rejected like four times for something i fixed three times ago, but dont take it personally, i completely understand you are probably trying to get through as many projects in as little time as possible and some things slip through the cracks

ok yall are really REALLY giving me hell about my pico usb placement and i have justified and explained how it will work like FOUR TIMES but im STILL REJECTED FOR IT so here we go again, if you reject me for this once again i swear to god i am going to just straight up leave this whole thing.

the board is suspended in the case:

<img width="401" height="281" alt="KeyboardSideView" src="https://github.com/user-attachments/assets/da044e0b-f85e-4bc2-a250-d01e0f6e88d0" />

the pico is attached to the bottom of the board. it is not colliding with the bottom of the case because the board is suspended. the usb can plug into the pico because the pico board has a thickness (1mm to be exact, specified by the datasheet here https://pip-assets.raspberrypi.com/categories/610-raspberry-pi-pico/documents/RP-008307-DS-3-pico-datasheet.pdf on page 7) and i have a usb plug that has a exterior thickness of less than 1mm, allowing it to fit between the pico and board:

<img width="417" height="366" alt="image" src="https://github.com/user-attachments/assets/3bfc97d6-8f07-42c6-adc3-ee172c833ecd" />

the cable will exit the case through the back. this is a top view of the cable exiting the board. the cable runs bellow the PCB. I reiterate, THE PCB IS SUSPENDED. THERE IS SPACE BENEATH IT. THE CABLE GOES IN THAT SPACE:

<img width="566" height="462" alt="image" src="https://github.com/user-attachments/assets/940a8b76-e6b8-45db-be5a-762635ebbbb8" />

this is a full side profile of the case. As you can see, the PCB is suspended by the key plate, the pico is soldered to the underside of the PCB, the cable plugs into the usb on the pcio, and the cable runs beneath the PCB and out of the case:

<img width="547" height="304" alt="image" src="https://github.com/user-attachments/assets/8129c6c5-171b-4af1-bbce-cc816e5abcef" />

THIS. WILL. WORK. I am 100% sure this will work. i have sextuple checked all of my work. everything fits. IT. WILL. WORK. if you are incapable of understanding that i recommend going to the local kindergarten and retaking shapes and colors instead of failing me based on your incompetence. 

Also, you marked off my BOM for not including a SINGLE 6.3mm THT resisitor. You can find this resistor in literally any electronics kit ever. breadboards come with them, arduinos come with them, even fucking leds come with them. they are everywhere. my school has a literal cabinet full of them. i have a few thousand of them. i would be willing to bet that you have at least a few hundred of them to. you could probably find them laying on the street, i probably have 3 on my floor somewhere, i wouldn't be surprised if i have one inside of my body. you can find this SINGLE component basically anywhere. you can barely even buy them individually. they cost like literally less than a cent. here is a pack of 2600 of them for like $15 https://www.amazon.com/dp/B085NQZNTY?lv=shuf&channelId=500&plpRedirect=mhFallback. I am (obviously) supplying this myself. whats next? do i have to include the solder i intend to use for this project in my BOM? the electricity i use for the soldering iron? the wires i use to patch things together? the usb cable i use to program the pcio? because all of those things have a significantly bigger impact on the total cost of this project. it is a SINGLE FUCKING RESISTOR. ITS NOT EVEN A NECESSARY COMPONENT, it just helps debounce the address line (which is only like 30mm long so it barely matters). the resistance dosent mater. it could be anywhere between a 220 and a 10k resistor. i could probably construct this component myself with a paperclip. like im sorry for the crash out but seriously is this the hill you are going to kill me on? 

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

also sorry about not fixing the issues with the PCB i fixed them but then forgot to commit, everything should be updated now.

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
