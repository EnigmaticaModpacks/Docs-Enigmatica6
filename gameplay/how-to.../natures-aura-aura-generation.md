---
cover: ../../.gitbook/assets/Enigmatica_6_1900x400.png
coverY: 0
---

# Nature's Aura: Aura Generation

## Aura

Doing much of anything with Nature's Aura requires consuming, well, Aura. Unlike coal for a furnace, Aura is simply everywhere and can be depleted with too much use.

Generating Aura, therefore, is essential. But some find the task a little daunting. Where to start?

Let's dive in and take a look at a few early game methods for creating Aura.

### **Canopy Diminisher**

![2021-03-28\_20 55 18](https://user-images.githubusercontent.com/9543430/112774689-66934e00-9008-11eb-804c-b1d84e98b65c.png)

Perhaps the earliest and cheapest Aura Generator, the Canopy Diminisher works by preventing the growth of 'big' oak trees. Any time one of these would grow in the area, the Diminisher instead converts it to Aura. Simple, right?

**What we need**

* Canopy Diminisher
* Imperceptible Builder
* A Chest or some other inventory
* An Item Frame
* Some way to cut down trees... More below

Below we see the area that the Canopy Diminisher will work in. Oak could be grown anywhere on this grid.

![2021-03-28\_21 11 54](https://user-images.githubusercontent.com/9543430/112775281-7c097780-900a-11eb-8e40-3b2bd499b584.png)

Automatically placing Oak Saplings can be accomplished simply with an Imperceptible Builder. This contraption will take items from the inventory above it and attempt to place them on nearby blocks. Specifying the block is done by placing the block in an Item Frame on the Builder itself. Below, there are Oak Saplings in the chest, and it's happily placing them on dirt in the area.

![2021-03-28\_21 19 54](https://user-images.githubusercontent.com/9543430/112775610-6052a100-900b-11eb-90c6-cf8b5f38acf2.png)

Now? We wait. Well, we still need to account for the eventual trees that will grow. So what options are available for cutting down the trees? Quite a few, but here are a couple that you might consider:

**Small Tree Cutter**

These handy machines will chop down entire trees in one operation. They don't require power but will run more quickly if powered. They also don't pick up the drops, so you'll need to manage that yourself.

![2021-03-28\_21 40 24](https://user-images.githubusercontent.com/9543430/112776656-42d30680-900e-11eb-8b55-473cc47980e5.png)

See it in action: [https://streamable.com/jur36w](https://streamable.com/jur36w)

**Pedestals with Tree Chopper Upgrades**

They start off a bit slow, but with a little enchanting they can cover a large area and chop everything quickly. They'll also take care of picking up the drops and transferring them to a chest if linked to another Pedestal with an Export Upgrade on it.

![2021-03-28\_21 39 46](https://user-images.githubusercontent.com/9543430/112776720-64cc8900-900e-11eb-8430-281d4d9d2619.png)

See it in action: [https://streamable.com/a9vyqu](https://streamable.com/a9vyqu)

**PneumaticCraft Harvest Drones**

Dumb Drones are available quite early with PneumaticCraft and offer a good amount of flexibility in builds. In particular Harvest and Collector Drones easily deal with a large area of trees. Of course, this can be greatly improved by programming your own drone!

Place the harvest drone down on a chest (sneak + right click) to bind it to that chest. It will pull hoes from this inventory which it uses to harvest crops and trees in the area. Be sure to restock the hoes. Place a charging station nearby with a Dispenser upgrade in it to give the Drone a place to recharge; it will seek out these charging stations automatically. Life and Standby Upgrades are recommended.

![2021-03-28\_22 02 32](https://user-images.githubusercontent.com/9543430/112777922-56cc3780-9011-11eb-8c41-898471b04427.png)

See it in action: [https://streamable.com/tkdw17](https://streamable.com/tkdw17)

**Ars Nouveau Fell Turrets**

Spell Turrets are pretty flexible tools for automation in Ars Nouveau. A simple spell consisting of **Projectile > Fell > Item Pickup** can be inscribed onto a Spell Turret to quickly chop any trees that grow and deposit the chests in an adjacent chest. These only fire with a Redstone pulse, but a bit of Redstone Dust and a Comparator can be used to detect when a tree grows, as shown below.

![2021-03-28\_22 22 30](https://user-images.githubusercontent.com/9543430/112779176-1cb06500-9014-11eb-824b-6ceb7c022519.png)

See it in action: https://streamable.com/foh8ze

### **Swamp Homi**

![2021-03-28\_20 29 27](https://user-images.githubusercontent.com/9543430/112779439-ba0b9900-9014-11eb-9a40-5998148fda50.png)

The Swamp Homi produces Aura by converting Mossy stone variants, such as Mossy Cobblestone or Mossy Stone Bricks to their clean counterpart. Therefore the trick to producing Aura with it is three-fold: Produce Mossy Cobble, place it, and remove the resulting plain Cobblestone.

The Homi covers only a small 5x5x5 area, but that's workable.

![2021-03-28\_20 31 37](https://user-images.githubusercontent.com/9543430/112779604-179fe580-9015-11eb-8ba3-e108cdb7a9e8.png)

Creating Mossy Cobblestone and similar blocks would normally require a vine farm and an auto crafter of some sort, but we've got a few other options here. Mekanism can convert Cobble to Mossy Cobble, for instance, in it's Metallurgic Infuser, and Thermal Series can as well with some Water and it's Fluid Encapsulator. However, perhaps easiest of all is the Pedestals Cobble Generator which produce different stones based on what's beneath them.

In this case, a vine below the pedestal will cause it to produce Mossy Cobblestone. Perfect!

**The Setup**

![2021-03-28\_22 38 49](https://user-images.githubusercontent.com/9543430/112780253-744fd000-9016-11eb-934e-542d8750b400.png)

**What we need:**

* One Swamp Homi
* One Pedestal
* One Cobble Generator Upgrade for the Pedestal
* One Vine
* Two Modular Routers
* One Puller MK1 Module
* One Placer Module
* One Breaker Module
* One Void Module

Setting this up should be pretty straight forward.

The Pedestal should be placed down first on a helper block, then remove the helper block. This allows the vine to be placed safely under it. Once ready, install the Cobble Generator Upgrade on the Pedestal.

The Modular Router adjacent to the Pedestal has the Puller and Placer modules in it set to pull from the Pedestal and Place below it. The second router is configured with the Breaker and Void Modules. Importantly, the Breaker module is set to blacklist Mossy Cobblestone. Feel free to keep the Cobble instead, by replacing the Void Module with a Sender Module linked to a large storage container.

This isn't the fastest setup, but it is very compact, which is excellent for tight quarters, such as setting it up under a Natural Altar.

Lastly, strongly consider an automatic turnoff for this contraption. An Aura Detector can be used to emit Redstone at a certain limit. Below is a very basic Redstone switch that disables the Breaker Router and the Pedestal. The Comparator on the Aura Detector reads the local level of Aura and the Comparator feeding into it is outputting 14 due to the number of items in the Dropper. Note that the Router is set to Low Redstone mode and the Comparators are in their default configuration.

![2021-03-28\_22 53 03](https://user-images.githubusercontent.com/9543430/112781204-613dff80-9018-11eb-8080-12ac8abf8692.png)

See it in action: [https://streamable.com/gup5b4](https://streamable.com/gup5b4)

### **Offshoot Observer**

![2021-03-28\_23 01 05](https://user-images.githubusercontent.com/9543430/112781806-926aff80-9019-11eb-8cec-39eb0234aeac.png)

This is more of a mid game Aura Generator as it requires access to the Nether just to craft, as well as for some of the extras we'll use. It works by generating Aura whenever slimes split. We can force that to happen pretty readily, however.

**The Setup**

![2021-03-28\_23 06 11](https://user-images.githubusercontent.com/9543430/112782084-3785d800-901a-11eb-8699-6d599224aaca.png)

**What we need:**

* One Offshoot Observer
* One Magma Cube Spawner
* A bunch of Wither Roses

That's a pretty short list, but some of these things can be hard to come by. Magma Cube Spawners can be found in the Nether in some Bastions and can be moved with Silk Touch or Cardboard Boxes. If one cannot be found, PneumaticCraft and Industrial Foregoing can both be used to spawn them instead.

The Wither Roses, however, might take a little more work since they're normally only obtained when the Wither boss kills another mob. Of course, growing more is quite a simple feat once the first has been found.

As the Spawner generates the Magma Cubes, they're inflicted with Withering by the Wither Roses and begin to take damage. They quickly split and then die, generating a nice amount of Aura.

Of course, we should still consider using an Aura Detector to disable the spawner when Aura is filled. If using a Vanilla Spawner, right click it with a Comparator to enable Redstone control. Some form of ranged item collection is also recommended as they will drop small amounts of Magma Cream as they die.

See it in action: [https://streamable.com/k792zr](https://streamable.com/k792zr)
