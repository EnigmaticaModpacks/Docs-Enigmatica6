---
cover: ../../.gitbook/assets/Enigmatica_6_1900x400.png
coverY: 0
---

# PneumaticCraft: Heating and Cooling

## Safe Compressor Usage

Besides pressure and explosions, PneumaticCraft has another major mechanic that raises more than a few questions: Heat Management.

Some blocks will heat up on use and become less efficient, others only work above certain temperatures, and others still need to be cooled below ambient heat to work. Let's take a look at the ways to handle all of this.

### Advanced Compressors

If you haven't already taken a look at compressors, now would be a good time to [brush up](https://github.com/NillerMedDild/Enigmatica6/wiki/PneumaticCraft:-Safe-Compressor-Usage). The basic ones, which max out at 5 bar of pressure, are great for machines like the Pressure Chamber or Assembly Table, but they aren't sufficient for powering a Pressurized Spawner or a suit of Pneumatic Armor. For these and other things, Advanced Compressors exist. With the higher pressures, however, comes a new challenge: Heat.

### Heating Things Up

Getting beyond basic compressors and machines will ultimately require Plastic to make Circuit Boards. Making Plastic, however, means first refining Oil in the Refinery.

![2021-03-31\_22 27 28](https://user-images.githubusercontent.com/9543430/113235028-64332d00-9270-11eb-99ee-cc2031771314.png)

The Refinery uses high heat to break down Oil into Diesel, Kerosene, Gasoline, and LPG, the last of which can than be converted into Plastic. But how do we supply the heat?

#### Vortex Tubes

![2021-03-31\_21 03 33](https://user-images.githubusercontent.com/9543430/113229281-a6ef0800-9264-11eb-9d40-94447ae2f147.png)

The Vortex Tube is a simple machine that uses swirling air to create a heat differential. In short, putting air in heats up the red side and cools down the blue side.

![2021-03-31\_22 40 27](https://user-images.githubusercontent.com/9543430/113236070-2e8f4380-9272-11eb-99ba-c8178887833d.png)

The two ends are thermally linked, however. As the blue side gets colder, so too does the hot side. To make the hot side as hot as possible, we need to warm up the cold side a bit.

#### Heat Sinks and Heat Pipes

By adding a Heat Sink to the cold side of the Vortex Tube, we increase the surface area, allowing more air contact. This in turn means the cold side warms up closer to ambient temperature.

![2021-03-31\_22 44 04](https://user-images.githubusercontent.com/9543430/113236337-a9f0f500-9272-11eb-83a4-4d8517240e63.png)

The biome does have a role to play here as well, with hot biomes like Deserts or Nether Locales contributing more heat than cold biomes. This testing world is a Void which is considered cool, so keep this in mind when building in your world.

There's only room for a single Heat Sink on the Vortex Tube, but we can extend this with Heat Pipe. Heat Pipe helps transmit heat towards cold blocks, leading to an equilibrium between a hot and cold block. Adding a few pieces of pipe and more Heat Sinks lets us raise the temperature of our system a bit more.

Heat Pipe can also help move Heat from the hot side of the Vortex Tube into the Refinery. This allows the Vortex Tube to be placed further away, which may help if space is limited.

![2021-03-31\_22 48 45](https://user-images.githubusercontent.com/9543430/113236683-59c66280-9273-11eb-875b-8b80d99078a8.png)

#### Insulation

You may notice that while the cold side is getting quite close to ambient, the hot side is not really increasing much. Well, we have the same effect going on there as we do with the Heat Sink on the other side. The Refinery itself is acting as a Heat Sink, losing heat to each air block it's touching.

Insulating the Refinery is simple enough: Cover it with any block that doesn't interact with the heat system. Therefore we can insulate it with nearly anything, including glass, pipes, trap doors, or leaves. Do note that some blocks are heat sensitive. Check uses on Heat Pipes in JEI to see a full list. But to offer an example, Lava will contribute it's heat into the refinery, at least until it cools off and turns into something else.

A good cheap insulation to use, however, is Thermal Lagging. These allow you to click through them while still insulating the block behind them, which is handy if you or a Drone needs to insert or extract fluids from the Refinery.

With insulation in place, we see our temperature start to soar.

![2021-03-31\_22 48 45](https://user-images.githubusercontent.com/9543430/113236683-59c66280-9273-11eb-875b-8b80d99078a8.png)

Of course, the process of refining oil will use this heat still, and with only 5 bar of pressure going into this Vortex Tube, the temperature will start to drop. One Vortex tube can easily keep the refinery above the required 100C, but adding more heat will also make the refining process faster.

#### Cross Mod Interactions

It should be noted at this point that PNC has some very much intended cross mod compatibility built into it when it comes to heat. Firstly, it's fully compatible with Mekanism's heat system. You likely won't be running a boiler with a Vortex Tube any time soon, but a Resistive Heater is a fantastic way of heating a Refinery, or any other block that needs heat.

Similarly, Immersive Engineering's External Heater can supply heat to attached PneumaticCraft blocks.

Lastly, while not _quite_ a cross mod interaction, if a heat pipe is connected to a Vanilla Furnace or Blast Furnace, it will power them, smelting any items in them. This can have interesting implications for mods such as Create.

### Cooling Things Down

So far we've focused on only one end of the spectrum and contentedly vented our cooling in the quest for heat. But the cold end of that Vortex Tube can be put to excellent use.

#### Heat Frames

![2021-03-31\_23 41 38](https://user-images.githubusercontent.com/9543430/113240537-eb859e00-927a-11eb-8206-920361f453cc.png)

Heat Frames can be installed on most any inventory with a right click. They effectively make that inventory heat sensitive, heating or cooling objects within. When heated, the items are smelted as they would be in a regular furnace. When cooled, however, some real fun begins. A number of fluids can be cooled this way such as Water to Ice, Lava to Obsidian, Molten Plastic to Plastic Sheets, and others that can be seen in JEI by checking the uses of the Heat Frame.

The same concepts from above here too. We need to insulate and vent the side of the vortex tube that we're not using.

![2021-03-31\_23 49 30](https://user-images.githubusercontent.com/9543430/113240982-cb0a1380-927b-11eb-9758-633e838b15c6.png)

Once it is sufficiently cold, simply drop a bucket (or tank) of fluid inside the inventory. It will begin to cool quite rapidly.

![2021-03-31\_23 50 20](https://user-images.githubusercontent.com/9543430/113241165-17edea00-927c-11eb-88de-9352ea45533e.png)

This process does require a lot of cooling, and therefore a lot of air. Additionally, some recipes will grant a bonus depending on how cold they are. Keeping the Heat Frame Cold enough to maintain that bonus will require more than 5 bar of pressure, which brings us to the next topic: Advanced Compressors.

### Advanced Compressors

So long as an advanced compressor remains below 50C, it will run at 100% fuel efficiency. However, for every mL of air generated, a certain amount of heat is also produced in the machine. This means better fuels such as Gasoline and LPG also generate more Heat per tick simply because they generate more Air per tick. Compressors will dissipate a bit of heat by themselves if left exposed to Air, but not nearly enough. The simplest way to expand this is the Heat Sink.

![2021-03-31\_21 50 14](https://user-images.githubusercontent.com/9543430/113232489-30093d80-926b-11eb-9125-2f5fea9a3aad.png)

Placed directly against a compressor, Heat Sinks can greatly increase the surface area, and thereby dissipate a lot more heat. Now, the compressor above is running LPG and has no Speed Upgrades. With only one Heat Sink, it's running at 71C or 93% efficiency. The same configuration without a Heat Sink results in a temperature of 185C and 55% efficiency.

Now between fuel input, air output, and Redstone control to keep the compressor running safely, that only leaves us three sides to work with. Adding two more Heat Sinks brings the temp back down below 50C. But if we want to speed it up, that's not going to suffice.

As previously discussed, Heat Pipes don't dissipate heat themselves, in fact they're insulated to _prevent_ heat loss. But they do move heat by attempting to find equilibrium between hot and cold. Therefore, we can use them as attachment points for more Heat Sinks.

![2021-03-31\_22 02 44](https://user-images.githubusercontent.com/9543430/113233423-2aacf280-926d-11eb-934e-bd1d08b1a591.png)

![2021-03-31\_22 02 59](https://user-images.githubusercontent.com/9543430/113233425-2bde1f80-926d-11eb-89a3-7040a5338180.png)

Adding just three heat pipes lets us bring our total Heat Sink count up from three to fifteen. This also lets us add three speed upgrades while remaining at 50C. Not bad, right?

Well... a compressor can hold 10 speed upgrades, generating quite a bit of air and heat in return. Cooling it with only Heat Sinks is going to be massive, costly, and eventually reaches a limit where heat pipes simply can't move heat away fast enough.

#### Air Grate Tube Modules

Great for pushing mobs around, Air Grate Tube Modules can also cool any Heat Sinks they're blowing against. Giving them more pressure allows them to reach more Heat Sinks, but even at just 0.6 bar they can be very effective.

![2021-04-01\_07 30 57](https://user-images.githubusercontent.com/9543430/113288422-f3fec880-92bc-11eb-89ea-c60a42552107.png)

Consider these two compressors. Both are burning LPG and have three Speed Upgrades. The one in the front has only a single Heat Sink on it and is at 144C. The one in the back, however has the same setup, but with the addition of an Air Grate pointed at the singular Heat Sink. That one is running at a cool 83C.

That's certainly a lot cooler. But that Air Grate at it's current 0.6 bar of pressure could be reaching a lot more than one Heat Sink. In fact, it would be able to reach a 5x5x5 cube of Heat Sinks.

![2021-04-01\_07 36 48](https://user-images.githubusercontent.com/9543430/113288476-06790200-92bd-11eb-9536-528360dd015d.png)

Expanding our setup out to 9 Heat Sinks with a single Air Grate brings our Compressor's heat down to a cool 45C; cooler than with 15 Heat Sinks passively radiating heat!

![2021-04-01\_07 40 44](https://user-images.githubusercontent.com/9543430/113289230-f44b9380-92bd-11eb-8ca5-a0f808d7766d.png)

Of course, nothing is stopping us from pointing more Air Grates at this setup. Or from re-configuring it so the Air Grates come into contact with more Heat Sinks. The setup shown below, for example, gets us to 49C with only five Heat Sinks. Each one is being cooled by the same air grate.

![2021-04-01\_07 46 49](https://user-images.githubusercontent.com/9543430/113289655-7b007080-92be-11eb-8e07-dc09ba80585f.png)

And adding a few more Air Grates brings the heat down even more to 41C:

![2021-04-01\_07 49 21](https://user-images.githubusercontent.com/9543430/113290027-0aa61f00-92bf-11eb-9dac-3affc5fc3e72.png)

#### Disclaimer:

The keen eyed-among you may have noticed the use of Creative Compressors by now. Rest assured, the same tests have been done with directly powering the Air Grate with the Compressor it is cooling and it is still very much worth it in terms of efficiency. The gains from cooling far outweigh the trivial air loss from running the Air Grates, which require 5mL/t plus 3mL/t for every three grates (rounded down) that they're cooling.

Active Cooling is also possible with Vortex Tubes, but they are far less efficient than a simple Air Grate and Heat Sink Combo.

Consider the setup below:

![2021-04-01\_09 01 08](https://user-images.githubusercontent.com/9543430/113297878-2ca49f00-92c9-11eb-8884-7d6443859926.png)

With ten speed Upgrades in it, it is running hot: about 320C when checked at around 10 bar of pressure. At that point it was running at 11% efficiency, producing 360 mL/t of air. Meanwhile the Vortex Tubes were consuming 212 mL/t of air. That's a net gain of 148 mL/t... Now compare that to the earlier Advanced Compressor with three Speed Upgrades and a single Heat Sink. That too was running hot, but much slower and produced 143 mL/t. So all this really manages to do is to burn fuel a lot faster.

In short, the Vortex Tube doesn't make for very efficient air production. It's best left for heating and cooling other machines.
