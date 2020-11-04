#About
I've always wanted to have a throttle panel for a twin engined plane, and this is my **WIP** design. I'm planning to have dual throttles and reversers, prop levers, and mixture levers; some likely candidates are a couple more levers to the sides for airbrake and flaps, and gear controls.

The gear design on [this (not mine) throttle panel](https://www.thingiverse.com/thing:4445717) I found and built a while ago is a very clean and clever design, but I disliked tha size and shape of the box overall. So I kept the multiplier gear idea and redid it from scratch to my liking.

Design is inspired on B737 and DH8C panels, so it's  a sort of Frankestein monster in between.

#Printing tips
* Parts are designed to minimize the amount of supports needed and have as much symmetrical parts as possible. Place the parts on their flat side and use supports anywhere needed.
* The holes on *support_singleaxis* need supports, but clearing them is a little hard)
* Infill for axis holders should be 35%, levers at 35 too so center of mass is near the axis, and the remaining parts are fine at 15-20%

#Electronics needed

* Switches:
  - EC11 rotary encoders
  - WH148 potentiometers (10K or 5K)
  - M20 microswitches
* Lots of dupont wires
* Arduino Leonardo

#Building tips
I recommend straping some sponge or cloth on the levers, so they have better grip.

#Software
Software side can be done with Arduino Joystick Library or MMJoy2. Not done yet
