---
cover: ../../.gitbook/assets/Enigmatica_6_1900x400.png
coverY: 0
---

# Powah: Automating the Energizing Orb

## Energizing

The Energizing Orb from Powah represents an automation challenge that is used in a few mods: Insert a precise number of items and provide power. The trick being the precision, since the machine can hold more than most recipes want.

The question comes up regularly on how to automate this simply. Let's go over a few options.

### Early Game Batch Crafting

There's no reason to wait on getting into Powah. It's available early on and even the basic Reactors represent an enormous amount of power. But one may not have all the infrastructure in place to automate this with something like Refined Storage, do let's just do some 'manual' batch crafting instead. The idea here is to be able to dump a lot of ingredients into a chest and walk away while things process. Pretty Pipes has a few features that will make this.

**What we need:**

* The Energizing Orb itself
* At least one Energizing Rod (feel free to make more, they will not go to waste!)
* Two chests or other inventories to act as input and output
* At least four sections of Pipe from Pretty Pipes
* Two Extraction Modules of any quality
* One Stack Limiter Module

This does require a piece of Quartz for that last item... but if you're clever you can find ways to obtain that without even needing to go to the Nether.

#### The Setup

![2021-03-27\_17 04 26](https://user-images.githubusercontent.com/9543430/112734818-81899380-8f1e-11eb-9c38-e731f4758852.png)

Above is the full system built, but there's a bit more that we can't see there. What do we do with those Pretty Pipes modules?

Choose a barrel to act as the input. For this, I've chosen the right hand side. Right click the section of pipe coming out of it with one of the Extraction Modules. This installs it in the pipe. To take a look at what's installed, right click that section of pipe again with an empty hand.

![2021-03-27\_17 07 20](https://user-images.githubusercontent.com/9543430/112734891-e9d87500-8f1e-11eb-900b-ee34e91a72fb.png)

Now, right click the Stack Limiter Module onto the pipe leading into the Energizing Orb. Right click again with an empty had as this one will need to be configured.

![2021-03-27\_17 08 59](https://user-images.githubusercontent.com/9543430/112734933-21dfb800-8f1f-11eb-8e88-dfd41f5dbf36.png)

We want to set this to a Maximum Item Amount of 1. This limit is _per item type_ meaning for each type of item we put into the input barrel, it will attempt to put one of each into the Energizing Orb. Handy, considering our very first tier of material requires 1x Iron Ingot and 1x Gold Ingot.

Now, to configure the output side. Again, simply right click the section of pipe coming out of the Energizing Orb with an Extraction Module. The Energizing Orb is a little 'smart' with the output, and only allows automation to extract a finished craft. So we don't need to filter this extraction at all. Great!

That's it! Batch crafting can now commence. As noted above, however, this can only handle one recipe type at a time. If we were to dump Iron, Gold, and Blaze Rods into the chest to batch craft both Energizing Steel and Blazing Crystals, Pretty Pipes would attempt to stick one of each in the Orb and the crafting would cease.

### Automation with Refined Storage

Batch Crafting is pretty decent, but we can do better. Requesting these items on demand with Refined Storage will make crafting a breeze. Pretty Pipes is still going to be integral to our automation, however, due to one of it's more interesting properties: Comparators can read the contents of the pipe.

#### The Setup

![2021-03-27\_17 24 36](https://user-images.githubusercontent.com/9543430/112735286-548ab000-8f21-11eb-8dac-a76f1ae8033c.png)

That's the entire system, but as before, there's a bit more going on under the hood. Let's have a look.

**What we need:**

* One Refined Storage System ready for [Auto Crafting](https://refinedmods.com/refined-storage/wiki/getting-started-with-autocrafting.html)
* One Refined Storage Crafter
* One Refined Storage Interface
* Some Pretty Pipes
* One High Extraction Module
* One High Speed Increase Module (optional)
* One Comparator

First, the Refined Storage Crafter itself has it's Crafting Mode set to "Redstone pulse inserts next set". This allows Refined Storage to insert a single set to begin, but only insert the next if the crafter receives a Redstone signal. So if we queue up more than one, it doesn't try to insert all of the items at once. Just one craft, then another with each pulse.

![2021-03-27\_17 28 43](https://user-images.githubusercontent.com/9543430/112735452-76386700-8f22-11eb-80f7-59c4adfcf039.png)

Next, the Pretty Pipe next to the Energizing Orb has both a High Extraction Module and a High Speed Increase Module installed in it. The Speed is optional, but the High Extraction Module is required. Why? We need to ensure that the Comparator only triggers once per craft. When crafting Nitro Crystals and Energized Steel, however, we get more than one output per operation. If we triggered the comparator for each item, it would break the system. The High Extraction Module ensures the entire stack is moved as a single unit, only triggering the Comparator once.

See it in action: [https://streamable.com/cs64x1](https://streamable.com/cs64x1)

### Alternatives

These are obviously not your only options, but they are among the simplest. You could, for instance, decide to go a little crazy and do all of this with PNC Drones or some wild Botania contraption. Those are beyond the scope of this article, but another early game option can be found in Industrial Foregoing.

#### The Setup

![2021-03-27\_17 47 22](https://user-images.githubusercontent.com/9543430/112735814-8e10ea80-8f24-11eb-9e3d-1ad964042a16.png)

Here we replace the entire Pretty Pipes portion of the previous automation with Industrial Foregoing Conveyor belts.

**What we need:**

* Three Conveyor Belts
* One Extraction Conveyor Upgrade
* One Insertion Conveyor Upgrade
* One Detection Conveyor Upgrade

This should need little explanation at this point. The Upgrades themselves are installed on the Conveyor Belts by right clicking with the upgrade item. The extraction and insertion pull from the Orb and insert into the Interface, respectively. And the Detection Upgrade causes the belt it's installed in to emit Redstone when items pass over it. This triggers the pulse needed to send the next set from RS.

The downside to a setup like this is that the conveyor can only extract 4 items at a time, meaning for something like Nitro Crystals which give 16, it'll trigger the Redstone pulse 4 times. While this isn't ideal, it still manages to craft most other recipes without issue. Finding a way to extend the pulse, or indeed finding other methods with the mods at hand, is an exercise left to the reader.
