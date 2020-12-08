#About
I've always wanted to have a throttle panel for a twin engined plane, and this is my **WIP** design. I'm planning to have dual throttles and reversers, prop levers, and mixture controls. Some extra controls which are very likely going to be made too are a couple more levers to the sides for airbrake and flaps, and maybe even landing gear controls and a trim wheel (but I might make them standalone, not yet that far on the designing process).

**EDIT**: *As of 20201203 Ive decided not to add more levers to this assembly. Im gonna make a separate, smaller, desk-fixed module for landing gear, flaps, spoilers and so on.*

The gear design on [this(not mine) throttle panel](https://www.thingiverse.com/thing:4445717) I found a while ago is a very clean and clever one, but after building it I disliked the size and shape of the box overall. So I kept the multiplier gear idea and reddid it from scratch to my liking.

Initial design is inspired on B737 and DH8C panels, so it's expected to end up as a Frankestein monster in between if you build it fully instead of just a couple modules.

There will be 2 variants for the thottles: a compound lever B737 style, and a more classic turboprop simple lever design, whose reversers are meant to be triggered by pulling back power.

#Variants
Levers are assembled by pairs, and can be mixed together: it's a modular design, so you can do whatever you like as all levers are interchangeable ;)

I'm not convinced by how the B737 throttles look next to the other ones, so I made a simpler variant without compound levers for throttle&reverse.

##Parts list:
### Main assembly
**You can mix a lever from one kind with a different one, as they are all built on the same specs. The following examples are for a pair of levers, both of the same kind.**

* Common (for every 2 levers):
	- support_singleaxis x1
	- support_doubleaxis x2
	- axis x2
	- small_gear x2
* B737 throttles:
	- lever x2
	- rev_lever x2
	- throttle_grip_main x2
	- throttle_grip_rev x2
	- cover_grip_main x2
	- cover_grip_rev x2
	- throttle_base x1
* Normal throttle levers:
	- lever_single x2
	- cover_grip_main_single x2
	- prop_base x1
* Propeller pitch levers:
	- lever2 x2
	- cover_grip_prop x2
	- prop_base x1
* Mixture levers:
	- lever3 x2
	- mixture_grip_cover x2 (sorry for not following the previous naming standard lol)
	- prop_base x1
* Case, qtys are for the 6 levers assembly:
	- base_clip x8 (4 for joining the lever bases, and 4 extra for the corners)
	- base_bracket2_leonardo x1 (goes on the back, and hosts the Arduino Leonardo)
	- base_bracket2_patch x1 (next to base_bracket2_leonardo, hosts the patch panel made for easier connections)
	- base_bracket2 x2 (front):
		+ No holes for buttons/toggle switches yet
	- base_bracket2_corner_LH x1
	- base_bracket2_corner_LH_back x1. Entry point for USB wire, hole has a separate part for covering it:
		+ usb_wire_cover
	- base_bracket2_corner_RH x1
	- base_bracket2_corner_RH_back x1
	- base_cover_big x2
	- base_cover_small x3
	- base_cover_corner x2
* Front covers: base model is base_bracket2. I'm also uploading some premade holes for my final design, which has battery/alternator/magneto and lights controls, shich are base_bracket2_A and base_bracket2_B.

#Wiring, components & electronics
It needs to be detected as an HID device, so you need to use MMJoy2 (some great English documentation [here](https://github.com/MMjoy/mmjoy_en)) or the [Arduino Joystick library](https://github.com/MHeironimus/ArduinoJoystickLibrary).

Most analog axis are based on 5K or 10K potentiometers (part no. WH148).

Position switches are some simple M20 microswitches. You will need to adjust their tips on some positions, and their usage is (as of 2020-11-16):

* Throttles on B737 version (with mounted reverser compound levers): reverse power enable
* Prop: feathering
* Mixture: fuel cutoff

You can wire everything with some Dupont terminated wires, soldering to the microswitches and bridging the shared buses (VCC & GND).

I'm using an Electrocookie board ([link](https://www.amazon.es/dp/B081R4YBY7), in case link or parts are nor available, dimensions are 39.5x44.5mm between hole centers) with soldered terminals and a 1N4148 diode for every node in the button matrix. Part named base_bracket2_patch hosts it.

#Printing tips
Parts are designed to favour interchangeability and symmetry between ENG1 and ENG2, so they are easier to replace.

**STL files are oriented randomly, please adjust side facing the bed so you get the least amount of overhanging area**. Their design makes pretty evident which side goes down, tho.

Infill is mostly done at 25%. I like the structural integrity of the hex infill pattern, so I do everything with this one.

Done with a Direct Drive printer and 1.75mm PLA. Used nozzle is 0.4mm wide andlayer height is set to 0.2mm.

#Building tips
Place some cloth or sponge between the lever axis and *support_singleaxis* for increased grip. Preferred for all levers, mandatory for the B737 style throttles as they are way heavier.

Chassis covers might need some trimming, as tolerances are quite tight.

Screws are M2 for microswitches and M3 for all remaining parts unless specified (various lengths).
