---
cover: ../../.gitbook/assets/Enigmatica_6_1900x400.png
coverY: 0
---

# Farmer's Delight: Automating Straw

Straw? Yes. Straw. This seemingly difficult to farm item used in making Canvas, Rope, Tatami, and Organic Compost is easier than one might suspect at a glance through JEI. There Rice appears to be the primary source, but a keener eye may notice it can be obtained by cutting grassy crops and plants with a knife. This includes plain old ordinary grass.

### Aura Field Generators

![2021-11-15\_15 52 48](https://user-images.githubusercontent.com/9543430/141852298-d2aa9fd1-ee63-42e9-aca6-3133d1235de6.png)

The humble Aura Field Generator will be the key to simplicity here. Certainly other methods exist that may work equally well, but few will be as simple.

The Aura Field Generator functions as a block breaker, instantly breaking any block that happens to find it's way between a linked pair. They require a little Aura to run, but nothing that can't be easily maintained with good [Aura Generation](natures-aura-aura-generation.md).

What's particularly special about Aura Field Generators, is their ability to be modified to use tools without using durability. Any block they interact with is broken exactly as if a player broke it holding whatever tool is in an item frame on one of the Field Generators. They'll even use the enchants on the tool, so Silk Touch or Fortune can be applied to a pickaxe, for example, to mine up ores from a Powder of the Bountiful Core farm.

![2021-11-15\_15 58 13](https://user-images.githubusercontent.com/9543430/141852959-852989a6-d1f4-40ac-b052-432c95bf1d5b.png)

We can make good use of this feature to break plain old grass as if holding a knife.

**The Setup:**

![2021-11-15\_15 43 33](https://user-images.githubusercontent.com/9543430/141853240-a2ebbe17-b5bd-446d-bca0-0409621dc339.png)

What we need:

* 10x Aura Field Generators
* 5x Item Frames
* 5x Knives (Flint Knife is fine, durability isn't an issue)
* A Hopper Enhancement
* 3x Hoppers
* Composter
* Some Pretty Pipes Pipe, Filters, and Extraction Modules
* Assorted inventories
* Dispenser
* Assorted Redstone components
* Timer

Above we see a rather simple setup, and there isn't much more to it than what's seen there.

To the left is Aura generation. This setup happens to be using the Firecracker Gaze for no particular reason than because it was simple to set up in Creative.

In the middle we have a small 5x5 area of grass and our Aura Field Generators. These break in a straight line and can be up to 10 blocks apart, so expanding this isn't too difficult if needed. In the back are our Item Frames and the Knives. Up front is a simple Redstone line to enable the Aura Field Generators; they only run with an active signal.

**Collection**

![2021-11-15\_15 44 20](https://user-images.githubusercontent.com/9543430/141854489-5cbc54a7-a9bb-4ac6-9188-59c487ba7bd4.png)

Off to the right is our collecting, processing, and input area. We see the Hopper Enhancement atop a vanilla Hopper. This picks up all items in a radius of about 7 blocks, placing them in the hopper below it; quite sufficient for our needs.

A pretty pipe is set to extract from the hopper directly since they can extract faster than a hopper can feed into another inventory. The first destination is a bin where our Straw is stored. This section of pipe has a filter allowing only Straw to enter the bin.

Heading up from there the leftover seeds are deposited into a barrel where they're fed down through a Composter to generate some extra Bone Meal. This outputs into a barrel which acts as our primary Bone Meal input. This section has a filter disallowing Straw. Note that the pipe has been manually disconnected from the hoppers by right clicking them with a pipe wrench. We don't want our stuff being inserted into the wrong inventory, after all.

Unseen below this is another section of Pretty Pipe extracting from the bottom of the Bone Meal barrel and feeding it into the Dispenser. The Dispenser itself is facing upwards such that it dispenses Bone Meal into the central block of the 5x5 area of grass, similar to a vanilla flower farm. Simply toss a timer on the dispenser to dispense Bone Meal every 40 ticks or so. It can go faster (the Aura Field Generators are very fast), but that will require more composters to realistically keep up with the incoming seeds. Bonus points for using a comparator to disable the timer when the Dispenser is empty.

Now all that needs doing is to load it up and turn it on. In testing, an initial input of 9 stacks of Bone Meal produced a healthy 4500 Straw with all of the seeds being converted to more Bone Meal to keep it running a bit longer.

See it in Action: [https://streamable.com/t6dyc7](https://streamable.com/t6dyc7)
