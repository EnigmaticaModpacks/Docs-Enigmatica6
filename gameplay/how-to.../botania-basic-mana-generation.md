---
cover: ../../.gitbook/assets/Enigmatica_6_1900x400.png
coverY: 0
---

# Botania: Basic Mana Generation

## Mana

Let's talk about mana, shall we?

Botania doesn't like to show you numbers and such, which is both a blessing and a curse. Much like Vanilla Redstone mechanics, it leaves it up to the player to figure it out, only laying out the basic rules. Some of us have an easier time with said rules than others. Ask me to build a CPU with Redstone and I'll just walk away, even though it's _entirely possible_.

This tends to frighten people away, especially in the beginning, as they simply have no idea where to start. So let's cover some basic mana generation.

The methods shown below are far from the only ways to do things. They aren't even necessarily optimal. And even though some alternatives are given, those lists are not exhaustive. Feel free to play with these examples and tweak them to your needs and capabilities.

### **Endoflames**

![2021-04-03\_14 53 24](https://user-images.githubusercontent.com/9543430/113488483-71c4fe80-948c-11eb-95b6-232d7c53237c.png)

Endoflames will likely be where you start with mana generation. They're decently inexpensive to craft and offer better returns than the alternative.

These flowers are pretty simple in terms of what they need:

1. Any furnace fuel
2. A place to send their mana
3. Time

They'll happily eat any burnable items that are dropped in the area and slowly convert them to mana. Once they've finished burning an item, they'll grab a new one.

**The Setup:**

![2021-04-03\_14 48 45](https://user-images.githubusercontent.com/9543430/113488753-eba9b780-948d-11eb-8288-450867726685.png)

What we need:

* Some Endoflames
* Pressure Plate
* Any Solid Block
* 2 Redstone Dust
* Mana Spreader
* Mana Pool
* Open Crate
* Hopper
* Fuel

Above we see a really basic setup of Endoflames being fed by an Open Crate, which drops any items it receives on the the ground.

The Endoflames themselves are placed at their very limits for reference. This is as far as they can be from the charcoal in the middle and still pick it up. Consequently the mana spreader is similarly as far as possible from the Endoflames. These can all move around as desired, however we're going to use this current orientation to our advantage.

So the way this is working is fairly simple. The Hopper is full of Charcoal and feeds it into the Open Crate, which consequently drops it on the pressure plate. The pressure plate then sends a signal along the dust and up the block, locking the hopper. This prevents it from spewing out all of the fuel on the ground. Not only is this server friendly, it also means your fuel isn't despawning before it's consumed.

But, what happens when the pool fills up? Well, it just slowly drops all the fuel, each piece despawning after five minutes and being replaced. That's no good, right? Let's fix that.

**The Setup:**

![2021-04-03\_15 24 43](https://user-images.githubusercontent.com/9543430/113489192-c5394b80-9490-11eb-9a01-8dfa5bdf04bc.png)

What we need:

* Some more solid blocks
* A bit more Redstone
* A Redstone Comparator
* A Redstone Repeater
* An Analog Lever

For anyone that's played Vanilla for a while, this shape may seem familiar: It's the same setup used for most Vanilla Filtering systems. Except here, we're using this as a master shut-off circuit for mana production.

The Comparator reads the fullness level of the mana pool and would output that as a signal down the line of Redstone. We're putting a limit on that, however:

![2021-04-03\_15 24 50](https://user-images.githubusercontent.com/9543430/113489200-cc605980-9490-11eb-99e1-ab2eb53ee3e5.png)

By sending a signal into the side of the Comparator, we're effectively telling the it "Only output a signal if your signal is greater than the signal from the side". In this case, the signal from the side is 14. This is handily provided by the Analog Lever which allows you to set an exact signal strength. It could also be provided with another comparator and an inventory mostly full of items.

This means, we'll only get a signal running down the line of Redstone if the pool is full. That runs down, powers the block that the repeater is against and which in turn relays the signal into our original circuit, locking the hopper and stopping production entirely.

![2021-04-03\_15 28 49](https://user-images.githubusercontent.com/9543430/113489271-4d1f5580-9491-11eb-9039-51432501c928.png)

And to get a bigger buffer of fuel, simply attach another hopper on the front, pointing into the first, and add a chest of some sort on top.

Now... yes, you can fit 45 flowers on the ground here. And _technically_ you could fit three more layers of floating flowers for a total of 180 around this... but you wouldn't right? Right?

Just like with FE generation, there are better ways than spamming Coal burning generators. Let's explore a few.

### **Rosa Arcana**

![2021-04-03\_15 50 59](https://user-images.githubusercontent.com/9543430/113489841-902ef800-9494-11eb-9df9-56751664c031.png)

Once you've mastered the Runic Altar and started generating some Runes, a couple new generating flora open up to you. One of the cheapest to make is the Rosa Arcana.

**The Setup:**

![2021-04-03\_16 18 00](https://user-images.githubusercontent.com/9543430/113490481-392b2200-9498-11eb-89c9-3e82ddb383ab.png)

The Rosa Arcana operates on a similar principle to the Endoflame. Rather than burning coal, however, it converts XP orbs to mana, and does so rather quickly. It's more efficient if it's pulling XP straight off of a player standing nearby, but we want this to run when we're off doing other things. Right?

This setup relies heavily on other mods in the pack. Cross mod interactions for the win!

What we need:

* Rosa Arcana
* Mana Spreader
* Mana Pool
* Redstone Comparator
* Redstone Repeater
* Analog Lever
* Some Redstone Dust
* Some Solid Blocks
* Mob Spawner
* Block of Coal
* Five Pedestals from the Pedestals mod and some Upgrades
  * Exp Magnet Upgrade
  * Exp Tank Upgrade
  * Exp Dropper Upgrade
  * Auto Attacker Upgrade
  * Export Upgrade
* Some inventory for storing drops

So, let's start with the actual Rosa Arcana setup. We see the same shut-off circuit as used for the Endoflames, so we won't cover that again. Just remember it's always best to turn things off when they're not needed. Especially things that are dropping items into the world. Pedestals are always on unless powered by a Redstone signal.

With Pedestals, orientation is important. Take note that the Pedestal under the Mana Spreader, which has the Exp Dropper Upgrade installed, is in fact upside down. This way the orbs drop down instead of being shot up and through the other blocks. Installing Upgrade coins onto Pedestals is as simple as a right click.

To the side of the Rosa Arcana setup is another Pedestal, this one with the Exp Tank Upgrade installed. This simply provides an extra buffer of XP and is, for the most part, optional. Link it to the Exp Dropper Pedestal with a Linking Tool: Hold the Linking tool in your hand and Sneak Right click the **receiving** Pedestal, then Sneak Right Click the **sending** Pedestal. So, start with the Dropper, then the Tank.

![2021-04-03\_16 35 00](https://user-images.githubusercontent.com/9543430/113490818-a17b0300-949a-11eb-95ff-9f82d4b68711.png)

Next up is the actual mob spawning area. Do note that Vanilla Spawners may be moved if broken with Silk Touch. Mekanism Cardboard Boxes also work, as does the Ars Nouveau Extract spell. So feel free to build this anywhere you like. Putting it under your base is a good way to have constant XP generation.

Apotheosis, the mod responsible for this mobility, also allows Spawners to be upgraded. Of note, sneak right clicking it with a Redstone Comparator will make the Spawner react to Redstone signals. Handy!

![2021-04-03\_16 37 44](https://user-images.githubusercontent.com/9543430/113490996-9e344700-949b-11eb-97dc-61b6f22b0cc4.png)

Pictured above is a simple spawn chamber. We won't discuss that any further here other than to mention Vector Plates which are what's being used to move the mobs around. What's important is the actual Pedestals.

First up, we have the Auto Attacker Pedestal directly in front of where the mobs come out. This attacks in an area, so exact placement isn't vital, but it was a handy way for me to stop the mobs from pouring out. By placing it on a Coal Block we are also filtering it so it won't attack us. This Pedestal will also act as item collection for us. It's linked to the Pedestal shown on the left which has the Export Upgrade installed. So all the drops are going into the inventory below that pedestal. Be sure to build in some overflow protection!

Next, to the right of the Auto Attacker is the Exp Magnet Pedestal. This quite simply picks up the XP orbs generated from killing the mobs. It's linked to the tank so that it's sending the XP to the Tank and the Tank sends to the Dropper. Optionally, Exp Relay Upgrades can be used to 'pipe' the XP even further. It really all depends on if you prefer moving XP or moving Mana.

That's the setup complete. Very lightweight and easy to build early on. The best part, however, is that this scales well. The Spawner can be replaced with either a Mob Duplicator or a Pressurized Spawner, both of which can spawn mobs incredibly quickly. All of the Pedestals Upgrade coins can be enchanted to speed them up and increase their range. The Auto Attacker Pedestal can even be given an enchanted sword to increase it's damage, give it looting, etc. To install the weapon, simply hold it in your off hand and right click the Pedestal with a Tool Swapper. And, of course, the Mana Spreader can be upgraded as well.

How far can you take it?

### **Gourmaryllis**

![2021-04-03\_17 09 23](https://user-images.githubusercontent.com/9543430/113491529-6929f380-949f-11eb-8f98-7ba4f64bad5d.png)

Another classic mana generator, the Gourmaryllis eats food and converts it to mana. Briefly, we want to feed it high value food and we want to alternate between two or more food items. It generates more Mana with greater diversity, remembering the last seven foods it was fed, so cycling through eight high quality foods would be optimal. Lastly, we _must_ wait until it has finished the first piece of food before dropping a second. If it's still processing the first, the second one will simply be destroyed.

Once again, we're going to lean on some extra mods to simplify this. Like all of the Botania flowers, it can be automated with only Botania and Vanilla mechanics, but it's OK to take shortcuts now and then.

For this setup, I'd recommend food items that rely strictly on grown crops. No, the Gourmaryllis isn't vegan. It's just simpler to automate food that doesn't rely on killing animals. Of course, feel free to use whatever foods you like. Vegetable Curry and Veggie Burgers are two pretty decent food items, however, that can be made from only crops.

This setup also won't focus much on the actual food automation. For that, Garden Cloches, Solar Insulators, fancy Create based farms, Sylph Farms, or many others are available and make the process of growing the crops simple. For the actual crafting, you can automate it with Refined Storage, Mekanism's Formulaic Assemblicator, an RFTools Crafter, or a Thermal Series Sequential Fabricator to name just a few options. There are many more.

**The Setup:**

![2021-04-03\_17 44 19](https://user-images.githubusercontent.com/9543430/113492305-81e8d800-94a4-11eb-9b96-d911bccd81e8.png)

What we need:

* Gourmaryllis
* Mana Spreader
* Mana Pool
* Mana Detector
* Some Redstone Dust
* Some Solid Blocks
* Two Redstone Comparators
* Redstone Torch
* Two Powered Toggle Latches
* Four Modular Routers
* Two Dropper Modules
* Two Puller Module MK1
* Two Sender Module MK2
* Two inventories of any kind

There's a lot more going on here than the previous automations. That's largely due to the extra conditions required by the Gourmaryllis. Let's set through it from start to end. This is not as complicated as it might seem.

First, the Gourmaryllis receives a piece of food. The first one is probably going to be hand delivered. This results in a stream of mana bursts being sent from the Spreader in the ground up through a Mana Detector and into a Mana Pool.

The mana detector simply outputs a Redstone Signal when it's receiving mana. This tends to flicker a bit, however, causing a pulsing redstone signal. That's no good for our needs, so we need to stabilize it a bit. We'll fall back to a simple Vanilla Redstone mechanic: The Comparator Decay Clock.

![2021-04-03\_18 02 22](https://user-images.githubusercontent.com/9543430/113492636-ce351780-94a6-11eb-8acc-719d5cacf17b.png)

When given a pulse on any of the Redstone Dust, these Decay clocks will pass the signal around in a loop, slowly loosing signal strength. Since it's constantly being refreshed by the pulsing of the Mana Detector, however it keeps outputting a constant signal to the right where it's disabling a Redstone Torch.

Once the signal decays, the Redstone Torch turns back on, powering the line of Redstone below. This sends a signal into the two Powered Toggle Latches.

These Latches are simplified Vanilla latches. When a signal comes in from the back, they toggle the output out the front. By setting them up with one on and the other off initially, we can have an alternating signal to power the two Modular Routers.

Finally, the Routers themselves are configured in Pulse activation mode with a Dropper Module.

As with the other automations, this one shuts off by itself. As soon as the mana pool fills, the spreader stops spreading and the last piece of food will leave a bit of mana in the spreader and the flower. So as soon as the pool starts accepting mana, the detector will send another pulse to get things moving again.

See it in action: [https://streamable.com/1vumbb](https://streamable.com/1vumbb)

The remaining routers have been off screen this entire time. They're simply set up to pull items from below them and send them to the dropper routers. So this is where you'd input food items from your automation.

![2021-04-03\_18 12 31](https://user-images.githubusercontent.com/9543430/113494644-29bbd100-94b8-11eb-9a29-aa22ff94821e.png)

### **Entropinnyum**

![2021-04-03\_20 30 59](https://user-images.githubusercontent.com/9543430/113494965-92587d00-94bb-11eb-8bbd-f07623c038f1.png)

The Entropinnyum is another that's available prior to opening the Alfheim Portal and as with each generating flora before it, it has it's own unique rules on how to use it. In this case, it absorbs an explosion from nearby TNT. So long as it's empty when the TNT goes off, the blast will do no damage.

As with the Gourmaryllis, the focus of this won't be the production of TNT. There are plenty of ways to do that that are easily discovered through JEI. Instead, we'll focus on making a safe chamber for the Entropinnyum to produce mana without blowing up your base.

**The Setup:**

![2021-04-03\_20 49 08](https://user-images.githubusercontent.com/9543430/113495253-45c27100-94be-11eb-8a0f-986001db12ae.png)

**View from above:**

![2021-04-03\_21 33 42](https://user-images.githubusercontent.com/9543430/113496121-6e4d6980-94c4-11eb-96bc-bbb12df17c2f.png)

What we need:

* Entropinnyum
* Mana Spreader
* Mana Detector
* Mana Pool
* Some Solid Blocks
* Some Redstone Dust
* Two Redstone Comparators
* Redstone Torch
* Blast Proof Blocks such as Obsidian or Hardened Glass
* Modular Router
  * Placer Module
  * Blast Upgrade
  * Detector Module

We've got our friends the Mana Detector and the Decay Clock back from our Gourmaryllis setup. They're a pretty handy combo for a lot of Botania related automation!

First thing, however, is to build containment for the TNT. Even with everything built 100% safe... we can never be too safe. And the last thing you want is for a stray TNT to go off and blow everything up. Our chamber is simple enough, it consists of a 3x3x3 box of blast proof blocks. Obsidian is easy to come by, but if you'd like something you can see through, Hardened Glass from Thermal Series is Blast Proof (and Wither Proof!).

In the back of the blast chamber is our Modular Router set to run on a pulse. This has the Blast Upgrade installed to make it immune to the TNT as well (just in case!), a Placer Module to put the TNT down in front of the router, and a Detector Module to light the TNT after placing it.

Another router can be used to send TNT into it since there isn't much room left for a pipe of any kind.

The rest is for controlling the placement of the TNT. Like the Gourmaryllis before it, we need to ensure the TNT is placed only when the Entropinnyum is empty. The simplest way to do that is to use the Mana Detector to determine when the mana spreader stops firing. Again, the decay clock ensures the signal from the Mana Detector remains stable for the duration of the firing sequence. And that line of redstone feeds into a Redstone Torch around the back. As soon as the mana stops firing, the torch is enabled, providing the pulse required to trigger the Modular Router.

Also like the Gourmaryllis, this circuit takes care of shutting off the system when the pool is full. There may be a single piece of TNT wasted at the end, but since it's been built safe, nothing will blow up.

There's a small problem with the build shown above: It doesn't work for more than one Entropinnyum. For that, we'll need to modify things a bit to trigger the router once for every flower we include.

To do this, we'll need a couple extra items:

* Sequencer from RFTools
* Nine Speed Upgrades for the Modular Router

You'll probably want a better mana spreader by now too, but that's optional still since this is all controlled through Mana Detection.

**The Setup**

![2021-04-03\_21 21 38](https://user-images.githubusercontent.com/9543430/113495965-1eba6e00-94c3-11eb-9377-5413bb84d746.png)

Around back, we've changed things a bit. The Redstone Torch has been moved back to make room for the Sequencer. The Sequencer is configure to run through it's sequence once when a new signal arrives. And that signal only arrives when the Spreader has stopped sending mana to the pool.

![2021-04-03\_21 31 51](https://user-images.githubusercontent.com/9543430/113496082-1282e080-94c4-11eb-9adb-f80b157bba1d.png)

The sequence itself is shown above. For anyone unfamiliar with the Sequencer, each white square represents an 'on' and each black square represents an 'off'. Therefore this will turn on and off eight times, once for each of the flowers we've placed nearby.

There are some extra options down below that are important as well. "Once1" means that the sequence will run through once completely when a signal is received. If a new signal comes in while it's running, it is ignored. The Delay is the number of ticks it waits at each square. So ours is sending a tick long pulse every two ticks. And the Sequence Length determines how many squares it will go through before it considers itself "done". In this case, at 16, it ends after the last square on the second row.

See it in action: [https://streamable.com/4td0hv](https://streamable.com/4td0hv)

### **Dandelifeon**

![2021-04-03\_21 59 39](https://user-images.githubusercontent.com/9543430/113496480-f5e8a780-94c7-11eb-8304-2f8ac64b34ac.png)

The Dandelifeon is an end-game mana generator based upon [Conway's Game of Life](https://en.wikipedia.org/wiki/Conway's\_Game\_of\_Life) and follows a similar set of rules. Those rules are detailed in the Lexica Botania and, as important as they are, we're going to mostly ignore them. The long and short of the process is that the Cellular Blocks we'll place on the board will multiply and die based on the blocks neighboring them, causing them to spread. The longer the cells live before reaching the Dandelifeon in the middle, the more mana they'll generate.

Why? Because as most anything on the internet, someone else has come up with an [optimal solution](https://www.reddit.com/r/botania/comments/5by0jl/optimal\_100round\_dandelifeon\_setup/).

So all we need to concern ourselves with is setting up the playing field.

**The Setup:**

![2021-04-03\_22 08 28](https://user-images.githubusercontent.com/9543430/113496592-38f74a80-94c9-11eb-8c42-1563532b289e.png)

As shown above, this flower requires a lot of room. The playing field is 25x25 to be exact, and the wall around it makes the entire build take up 27x27 blocks.

The beauty of this build is the efficiency. Yes, Entropinnyums and Rosa Arcana can output more mana per tick. But this is no slouch and generates an enormous amount of mana for very little. Just six cellular blocks, or 2 beets, 2 carrots, 2 potatoes, and 6 cactus. That's... cheap.

We'll also be using a timing system to control this, rather than a mana based system. The reasoning is simple: We know exactly how long it takes to play the game, and we ideally want to start it running again the moment it has finished, rather than once the mana has fully drained from the flower. This being an end game flower, pulling all the mana out quickly shouldn't be an issue. Gaia Spreaders are available at this point.

As for the timing, the game lasts 100 rounds. Each round is half a second. Therefore a full game runs 50 seconds or 1000 game ticks.

What we need:

* Dandelifeon
* Mana Spreader
* Mana Pool
* RFTools Timer
* PneumaticCraft Pressure Tubes
* PneumaticCraft Redstone Modules
* Six Modular Routers
  * Six Placer Modules
  * Six Sync Upgrades
* Two Levers

First, the Modular Routers are placed as shown above. These are responsible for placing the Cellular Blocks, so each one will be given a Placer Module configured to place the blocks in the Up direction. Now, for this to work properly, they must all place the blocks in the same game tick. Thankfully Modular Routers has a solution to this: The Sync Upgrade. Any routers with a Sync Upgrade set to the same channel installed in them will all fire in the exact same game tick. To configure a channel, hold the stack of six and right click the air. Pick any number and they'll all be configured to that channel. Place one in each and then set them all to Redstone Pulse mode.

Next, the redstone itself. For this we'll use a new trick: PneumaticCraft Redstone Modules. These turn regular old Pressure Tubes into Redstone Conduits. Meaning we can take a signal in and send it to multiple output locations without worrying about signal decay. 15 in means 15 out. They can do a lot more than this, but for our setup here, that's all we need.

![2021-04-03\_22 42 26](https://user-images.githubusercontent.com/9543430/113497056-f08e5b80-94cd-11eb-819f-c27667bb3df5.png)

Simply run the tubes so they reach under each of the Modular Routers and then place a Redstone Module on top of each tube under a Router. The default settings are fine.

The RFTools Timer will take care of the input signal.

![2021-04-03\_22 44 38](https://user-images.githubusercontent.com/9543430/113497092-4fec6b80-94ce-11eb-9b52-dee71f1491b2.png)

Run the pipes up and place a Redstone Module facing into the orange arrow of the Timer. Right click the Module with an empty hand and click the Red Arrow in the GUI to change it to Receive mode.

The Timer should be set to "Pause while Redstone active" with a delay of 1000. The Pause option will stop the timer once a redstone signal is received on the blue arrow side of the timer. For now, our Lever will act as an off switch.

With the Routers filled with Cellular blocks (ideally sent via another Router with a Distributor Module installed) only one thing remains: The Dandelifeon flower itself only operates when it's receiving a Redstone signal. For this, we'll just put a Lever under the block it's on and power it. Since the placement of the Cellular Blocks all happen in the same game tick, there's no reason to turn this off and on.

Of course, we like things to shut off on their own, right?

So we'll use some of our previous tools to get that done here too:

![2021-04-03\_22 59 20](https://user-images.githubusercontent.com/9543430/113497294-b5d9f280-94d0-11eb-968e-b58eb054c357.png)

What we need:

* Two Redstone Modules
* More Pressure Tubes
* Redstone Comparator
* Analog Lever
* Redstone Dust

As in our earlier automations, the Comparator will read the level of the pool. With the help of the Analog Lever set to output a signal of 14, it will only output once full. The Redstone Modules are then used to transmit the signal over the game board to the timer, where the signal pauses the timer.

Watch it in action: [https://streamable.com/hhl222](https://streamable.com/hhl222)
