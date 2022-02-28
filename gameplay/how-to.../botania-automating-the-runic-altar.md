---
cover: ../../.gitbook/assets/Enigmatica_6_1900x400.png
coverY: 0
---

# Botania: Automating the Runic Altar

## **Runic Altar**

![2021-04-03\_23 59 06](https://user-images.githubusercontent.com/9543430/113498185-a1015d00-94d8-11eb-9d89-cd9f31520714.png)

The Runic Altar is a pain point for many players learning Botania. Without other mods, it represents a decent challenge. With other mods, however, the challenge is significantly reduced.

### **Refined Storage Crafting**

We won't cover the basics of Refined Storage here. Auto crafting is covered in detail [here](https://refinedmods.com/refined-storage/wiki/getting-started-with-autocrafting.html). So I'll assume you already have a working Refined Storage Crafting system.

**The Setup:**

![2021-04-04\_00 35 02](https://user-images.githubusercontent.com/9543430/113498886-fb9db780-94de-11eb-9cf7-f8c5fcbd0a38.png)

What we need:

* Runic Altar
* Mana Spreader
* Mana Pool with some source of Mana
* Open Crate
* Barrel
* Three Modular Routers
  * Puller Module MK1
  * Two Sender Module MK2
  * Vacuum Module
  * Activator Module
* Iron Crafter from Extra Storage
* Redstone Comparator
* Adjustable Repeater from Create
* Solid Block
* Wand of the Forest

So, the crafter itself is loaded with our patterns. An Iron Crafter was used here to fit all of the patterns. Of course, two regular Crafters could be chained for the same effect. Critically, the Crafter is set to Pulse mode. It is facing into the barrel which acts as an intermediary for the Modular Router.

A note on the patterns. Each one includes all of the items for the Rune, including the Living Rock and catalyst Runes used in higher tiers. This does mean that if multiple Runes of Envy (for example) are queued, the system will require 1 Water and 1 Spring for each. There are other ways to do this that are less wasteful, but this is meant to be a simple system.

Being in pulse mode, the crafter will output exactly one set of ingredients, then nothing until it receives a pulse.

Router A is configured with a Puller Module MK1, set to pull from Down. It also has a Sender Module MK2 which sends over to the Open Crate. Since this is in direct line with the Crate, an MK1 module could be used instead if necessary. This gets our ingredients onto the altar where they'll begin to craft. Since there are no timing circuits, this can take as long as it needs, though it does need to complete before the Living Rock despawns!

Router C has the Activator Module and the Wand of the Forest in it. The Module is set to Front, Action: Right-click item in buffer. This just continuously uses the wand on the altar. Once the required mana has actually been transferred, this will finish the craft with a right click of the wand.

Router B and the Redstone components in front of it are the real heart of this system.

First, it's important to know that the Comparator on the Runic Altar gets treated specially by Botania. While the Altar is receiving mana, it will output a signal of 1. Once it's ready to craft, it will output a signal of 2. We'll use that signal a little differently than it was intended, however.

Once the mana starts transferring, our Comparator turns on, powering the Adjustable Repeater. These repeaters can be adjusted to any signal delay, unlike Vanilla Repeaters which cap out at 4 ticks. Ours is set to 3 seconds. We'll come back to that delay in a moment. For now, just understand that it's powering the Oak Planks, thus providing a signal to both the Crafter and Router B.

Router B is in turn configured with a Vacuum Module which is filtered to blacklist Living Rock. It also has a Sender Module MK2 linked to the Refined Storage Interface. Finally, it's is set to Redstone High mode.

So while the Altar is crafting, Router B is activated and attempting to vacuum up anything it can. The only thing that remains in world, however, is the Living Rock, hence the blacklist. The 3 second delay on the Repeater keeps this active for long enough to gather the crafted Rune and any of the catalyst Runes that are returned after a craft. Three seconds is just enough for any of the crafts. Optional Speed Upgrades in the Router mean this delay can be lowered if desired.

Finally, when that Repeater turns off, the Crafter effectively receives it's pulse, allowing it to insert the next set of ingredients and continue the cycle.

See it in action: [https://streamable.com/zt76lw](https://streamable.com/zt76lw)
