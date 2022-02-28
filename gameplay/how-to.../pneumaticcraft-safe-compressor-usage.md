---
cover: ../../.gitbook/assets/Enigmatica_6_1900x400.png
coverY: 0
---

# PneumaticCraft: Safe Compressor Usage

## Compressed Air

Generating 'power' or compressed air in PneumaticCraft (PNC) involves a little bit more planning and thought compared to basic FE generators. This coupled with the fact that machines will burst if over pressure tends to frighten some folks away.

Worry not. This can be done safely. Let's demystify this a bit.

### The Pressure Chamber

The first machines used in PNC are the Pressure Chamber and the Air Compressor. These are connected with Pressure Tubes as shown below.

![2021-03-27\_14 44 18](https://user-images.githubusercontent.com/9543430/112731244-6877e700-8f0c-11eb-8e63-fe2fde2d0f64.png)

The Pressure Chamber itself is a simple 3x3x3 hollow cube that consists of the following:

* Pressure Chamber Walls
* Pressure Chamber Glass (optionally used in place of Walls)
* Two or more Pressure Chamber Interfaces for inserting and extracting items for crafting
* Pressure Chamber Valve, which is where the Pressure Tubes connect to the machine.

It may optionally be 4x4x4 or 5x5x5, granting it greater volume for holding air. This may not be desirable early on since the Chamber must reach a minimum pressure before it can craft. Higher volumes mean more air is required to reach that pressure and therefore filling it will take more time.

Here we can see the Interfaces; one in input mode (right) and one in output mode (left). The mode is determined by the way they're placed. A Pneumatic Wrench may be used to rotate them, however.

![2021-03-27\_14 44 24](https://user-images.githubusercontent.com/9543430/112731245-6877e700-8f0c-11eb-9ac5-3331af226732.png)

### Compressing Air and Basic Control

The Compressor itself is a simple machine that accepts any Furnace Fuel (except buckets of fuel such as lava or LPG) to produce air. By default, it will simply run until it expends all of it's fuel or until it bursts, whichever comes first.

But we don't want that now, do we?

The very first thing to do here will be to install a safety valve of some sort. The Security Upgrade serves this exact purpose.

![2021-03-27\_15 22 50](https://user-images.githubusercontent.com/9543430/112732432-51d38f00-8f10-11eb-9f14-9959c8011f56.png)

Simply placing it in the Upgrade Slots in the upper left corner of the Compressor's GUI handily resolves the problem of bursting machines. Now, this will simply vent air when it's dangerously full.

But that's wasteful. Now it's simply going to run until it runs out of fuel, venting any excess air it makes in the process.

Solving this requires a little bit of math and some basic Redstone knowledge. If we take a look at the Pressure Gauge Tube Module, we'll see what sort of math we're dealing with:

![crop2021-03-27\_14 45 59](https://user-images.githubusercontent.com/9543430/112732548-01106600-8f11-11eb-99e2-92f9d6eeced4.png)

So the Redstone signal strength equals two times the pressure in the tube this module is attached to. Now, if we remember that Redstone signals drop off by one level per block, we can use these two features to build a line of Redstone that is exactly signal 1 at the compressor when the pressure is a nice safe 4.5 bar.

4.5 bar x 2 = 9, so the Redstone line needs to be 9 dust long. There are a lot of creative ways to accomplish this, but the simplest is a length of dust and a repeater as shown below.

![2021-03-27\_15 39 07](https://user-images.githubusercontent.com/9543430/112732871-fd7dde80-8f12-11eb-9891-71cda93adeef.png)

This little loop will result in the Compressor getting a Redstone signal just as the tube reaches 4.5 bar, which is more than sufficient for any early crafting.

The final step is to ensure the Compressor is set to be enabled only without a Redstone signal. Set it to "Enable on Low Signal" in the GUI.

![2021-03-27\_14 47 26](https://user-images.githubusercontent.com/9543430/112732914-34ec8b00-8f13-11eb-8f02-c5b25b6fe3dc.png)

Now, you may notice something a little alarming at this point: Your Compressor isn't actually turning off at 4.5 bar. Why? Well, Solid Fuel has a little bit of a drawback here. You can't stop burning it mid way through. So the Compressor will continue to burn whatever piece of fuel it is currently working with before shutting off. If it has some long lasting fuel like Coal Blocks or Blaze Rods, it might actually keep burning for a while before it shuts down. The Security Upgrade will cover those scenarios but, again, this is wasteful.

There ultimately are two ways of dealing with this. First, increase the volume of the network, which can be accomplished by adding more machines or by inserting Volume Upgrades in existing machines. Second, move on from Solid fuels and upgrade to a Liquid Compressor. Enigmatica 6 adds a lot of extra fuels to the Liquid Compressor, so finding a renewable fuel source shouldn't be too difficult, even early on. A complete list is available in game in the Available Fuels tab of the Liquid Compressor's GUI.

### Advanced Redstone Control

Not everyone likes Vanilla Redstone. It's prone to breaking when water is involved and, in general, just takes up a lot of space. As it happens, PNC includes it's own system for transmitting Redstone signals, and has some very advanced Logic operations it can perform.

We'll keep this simple, however. It's just a shut-off circuit, after all.

What we need:

* Two Redstone Modules
* Some more Pressure Tubes
* One Advanced PCB

Advanced PCBs can be installed on many Tube Modules to enhance their base functionality. Install one on the Pressure Gauge Tube Module by right clicking the module with the PCB. It will turn green to show that the upgrade has worked. Right click the module again to see it's new GUI.

![2021-03-27\_16 03 00](https://user-images.githubusercontent.com/9543430/112733459-92cea200-8f16-11eb-9bc0-48549f11d5f1.png)

That's not going to do much though. Let's change that up a little:

![2021-03-27\_16 03 30](https://user-images.githubusercontent.com/9543430/112733377-1f2c9500-8f16-11eb-9aef-7adf537786db.png)

Now we'll get a signal whenever the pressure in the tube is less than 4.5 bar.

Next, we need to transmit it. Redstone Modules are installed on tubes like other Tube Modules and turn the entire tube network into a potential Redstone network. Multiple colored channels exist and each module may be used to receive or emit a signal, among other things. Advanced PCBs make these really powerful but we're keeping this simple. Explore those options on your own.

![2021-03-27\_16 09 25](https://user-images.githubusercontent.com/9543430/112733554-040e5500-8f17-11eb-950f-a5e89ccb3657.png)

The Redstone Module facing the Pressure Gauge is set to Receive mode. To toggle the mode, right click the Module and click the red arrow. A Pneumatic Wrench will also toggle the mode.

![2021-03-27\_16 09 32](https://user-images.githubusercontent.com/9543430/112733660-a3cbe300-8f17-11eb-9fdc-0306624341a3.png)

The Module facing into the Compressor is in the default 'emitting' configuration.

Finally, we need to reverse the Redstone mode in the Compressor itself. Set it to Enable on High Signal, since we're now emitting a signal only when pressure is below our threshold.

![2021-03-27\_16 23 07](https://user-images.githubusercontent.com/9543430/112733863-bc88c880-8f18-11eb-8422-5044dc5ac8da.png)

This last bit may seem like an odd little distinction to make, but there's an excellent reason for it. When the game is loading, these Redstone signals aren't always processed before machines begin working. By having the Compressor only work with a high signal, it means it's off by default since there cannot be a signal here until the entire system has come online and pressure is being read. Inverting this logic can result in the compressor running briefly during startup, even if the machine is already at or above the threshold... which could mean your compressor bursts before you even have a chance to do anything about it. Again, the Security Upgrade helps here, but we can also build things to be safe by default.

With the above setup, Liquid Compressors will run very safely even at high speed and high thresholds since we're measuring off of the very first tube in the system. A Liquid Compressor burning LPG with 10 Speed Upgrades, 25 Volume Upgrades, and configured to run below 4.9 bar, will generate air exceptionally quickly without ever triggering the Safety Upgrade. That makes these ideal for running 5 bar machines such as the Pressure Chamber or Assembly Table at max speed, which is great when it comes to advanced PNC crafts.
