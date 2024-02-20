# 45 - Mechanical Bits

Through all the Engineering pages I've focused on electrical and programming solutions, because those are what I know, but they are not always the right answer. For example, in [this Reddit post](https://www.reddit.com/r/arduino/comments/s0jnh9/what_kind_of_motor_can_i_use_for_this_i_need_a/) the author asks **"What kind of motor can I use for this? I need a lightweight pole to go from 0 to 90 degrees [as fast as possible]?"** and the answer really stuck out to me

{{< quote "[u/olderaccount](https://www.reddit.com/r/arduino/comments/s0jnh9/comment/hs2kewi/?utm_source=share&utm_medium=web2x&context=3)" >}}

If you really want fast. Go stored kinetic energy with sudden release.

You can use a motor or other energy source to build up the kinetic energy in some elastic material.

A simple catapult, if you will. If you don't want old school, you can store your energy in a pneumatic system. A valve controlling how much can go into the cylinder at once would control your speed.

Failing that, electromagnetic (like a solenoid) will probably be fastest.

{{< /quote >}}

Now, if you've actually read through these guides in order, you'd know there's a lot of complexity hidden in that answer. You might need a PID (see {{< button relref="/Engineering/Signals/controlsys" >}}Control Systems{{< /button >}}) to compensate the system to behave as you want still, but the point remains- you shouldn't look to solve problems solely with fancier electrical parts: use everything you've got. While code on a microcontroller can do a lot, at the end of the day, you'll still need to interface back to reality - and that means hacking away at real materials, using tension in springs, moving gears, etc.

I absolutely do not have the expertise to teach about these things, so instead I'll do my best to link to resources I find

## Gears

[Openscad Gears Library](https://github.com/chrisspen/gears) (or [This one](https://github.com/dpellegr/PolyGear)) 

https://woodgears.ca/gear_cutting/index.html (or the better, [standalone version](https://woodgears.ca/gear/index.html))



## Springs/Dampening

## Belts

## Thermals

## Materials

### Metals

Corrorision, weldability, etc.

### Elasticity



## Vibration

## Hydraulics & Pneumatics

### Pumps

### Valves

### Viscosity

## Fuels

### Lubrication



# Thinking Outside the box

[Big LED Matrix Becomes Tiny LED matrix Thanks to Fiber Optics (Hackaday, Elliotmade)](https://hackaday.com/2022/03/01/big-led-matrix-becomes-tiny-led-matrix-thanks-to-fiber-optics/)

