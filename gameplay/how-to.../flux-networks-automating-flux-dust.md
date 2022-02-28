---
cover: ../../.gitbook/assets/Enigmatica_6_1900x400.png
coverY: 0
---

# Flux Networks: Automating Flux Dust

## Flux Dust

Creating Flux Dust has gone through several iterations during the life of the Flux Networks mods. In it's current iteration, we are presented with a rather informative graphic depicting the in-world process:

![2021-04-05\_20 29 11](https://user-images.githubusercontent.com/9543430/113642393-b8158b80-964d-11eb-80eb-597ac0a5a7e7.png)

Drop some Redstone Dust on Bedrock or a Flux Block, place an Obsidian in the block space above the Redstone, and finally punch the Obsidian.

Ouch. Seems a bit rough on the hands.

But the effect is immediately apparent. The Obsidian crashes down and converts our Redstone into Flux.

Now, how to avoid ever doing that again?

**The Setup:**

![2021-04-05\_20 26 34](https://user-images.githubusercontent.com/9543430/113643079-68d05a80-964f-11eb-9896-7059b179a27a.png)

What we need:

* Flux Block
* Some Obsidian
* Some Redstone Dust
* Four Modular Routers
  * Placer Module
  * Breaker Module (Made with a Diamond Pickaxe or better)
  * 2x Sender Module MK1
  * Void Module
  * Puller Module MK1
  * Dropper Module
  * Vacuum Module
  * 12x Stack Upgrades
* Deployer

First, a note. Sometimes the Obsidian is lost during this process and is replaced with Cobblestone. That poses a problem that's easily resolved, however. But for now, be aware that it may be wise to set up a simple Obsidian farm of some sort. There are a number of ways to go about that, however, let JEI be your guide.

**Modular Router A**

![2021-04-05\_20 48 23](https://user-images.githubusercontent.com/9543430/113643546-8e119880-9650-11eb-9f0d-43d8072f961a.png)

This responsible for placing the Obsidian each cycle, and as such is configured with the Placer Module set to _Direction: Right_

**Modular Router B**

![2021-04-05\_20 48 55](https://user-images.githubusercontent.com/9543430/113643550-8fdb5c00-9650-11eb-8d04-a53e78a9ff1e.png)

This is our breaker. Since we're dealing with Obsidian, the Breaker Module must have been crafted with a Diamond Pickaxe or better. Otherwise it's going to sit there looking at us funny.

The Sender is configured to send only Obsidian up to Router A. The Void Module takes care of the pesky Cobblestone. Poof.

**Modular Router C**

![2021-04-05\_20 48 57](https://user-images.githubusercontent.com/9543430/113643556-910c8900-9650-11eb-99e3-09dfe15e8500.png)

This one deals with dropping the Redstone Dust which it pulls from an adjacent inventory. The dropper is simply configured to go to the left, onto the Flux Block.

**Modular Router D**

![2021-04-05\_20 49 00](https://user-images.githubusercontent.com/9543430/113643559-936ee300-9650-11eb-9db1-c5d83fd806f0.png)

And here we have our collection router. The Vacuum Module is left on the default _Direction: All_ setting, but is filtered to Whitelist Flux Dust. This prevents it from accidentally picking up our Redstone Dust before it can convert.

Now the only thing that remains: The Left Click.

As it happens, this is a rare feature among mods. Our options here are limited. However, Create's Deployers are reasonably accessible and easy to work with. This setup will function just fine with the Deployer being powered by an Encased Fan and a Magma Block, for instance.

In order to simulate a left click, the mode of the Deployer must be changed from the default "Jabby Finger" to the "Punchy Fist". Simply right click the side of the machine with the hand coming out of it to change the mode. Right clicking any other side will only rotate it!

Another option would be a Player Simulator from Integrated Tunnels. As mentioned, this is a rare feature in mods.

See it in Action: [https://streamable.com/v7ft85](https://streamable.com/v7ft85)
