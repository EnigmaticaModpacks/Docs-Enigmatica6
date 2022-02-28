---
cover: ../../.gitbook/assets/Enigmatica_6_1900x400.png
coverY: 0
---

# Mekanism

## **Developer Notes**

We've modified Mekanism's Energy generation quite a bit to make it's advantage over other mods smaller.

We implemented these changes in these Pull Requests:

* [https://github.com/NillerMedDild/Enigmatica6/pull/1125](https://github.com/NillerMedDild/Enigmatica6/pull/1125)
* [https://github.com/NillerMedDild/Enigmatica6/pull/1312](https://github.com/NillerMedDild/Enigmatica6/pull/1312)
* [https://github.com/NillerMedDild/Enigmatica6/pull/1665](https://github.com/NillerMedDild/Enigmatica6/pull/1665)

## **Ethylene**

**TL;DR: Energy and Time cost to produce Ethylene Increased**

These values end up allowing a single PRC producing Ethylene at top speed to consistently produce up to 3.2k rf/t in the Gas Burning Generator. This is with fully upgraded machines. Starting off the rates will be much slower/lower.

The rate of production is slowed substantially, meaning that the PRC is only capable of producing enough to keep a GBG running at 0.5 mb/t. This gives nice consistent power while allowing ethylene to serve as a dense power storage medium. It still retains it's high burn rate if enough can be supplied, up to \~70k rf/t.

The cost of production is brought up to help balance out the numbers while keeping the production speed reasonable. Overall, it costs about 2.4k rf/t to produce per PRC and burns for about 5.6k rf/t if burned as quickly as it is produced. About thirteen upgraded PRCs would be required to maintain the maximum burn rate of a single Gas Burning Generator.

| Generator             | Output per 1000 mb (MFE) | Burst Rate (FE/t) | Net Average Rate (FE/t) |
| --------------------- | :----------------------: | :---------------: | :---------------------: |
| Gas Burning Generator |        11,260,000        |       72,190      |          3,200          |

## **Fission and Fusion**

Energy per mb of Steam is reduced. This has a heavy impact on fission burn rate. Since less steam is produced, less water is recycled for cooling. Reactors will explode if they're running near their previous limits and do not have appropriate safety measures in place.

For instance, with the default configs, the basic fission reactor and turbine we provide in schematics produces 570k rf/t and can run at a burn rate of 20mb/t. It now runs stable at around 4mb/t and produces 114k rf/t. That's a pretty good step up from Powah reactors still, but a bit more in line.

Waste Decay Rate substantially increased, ultimately just meaning that fewer barrels are required in the world to handle dissipating the waste from a larger reactor. This should be helpful for those looking to build a permanent power infrastructure based on fission.

Fusion similarly sees a big hit from the steam change as well as a reduction in it's base power by a factor of 10. Passive generation is also significantly reduced, meaning a turbine is required to get the most energy out of Fusion.

Water cooled fusion generates enough steam to run a single max sized turbine at about 40% flow rate, generating another 3.18 million RF/t.

Of course, Fusion can still go a lot higher than this by pumping in D-T fuel. One Chemical Infuser making D-T as fast as it can (burning 204krf/t) was enough to create more steam than that max sized turbine can handle, bringing the previous 3.18 m rf/t up to over 8.82 m rf/t. So if people do want to get crazy still, they can, but it requires heavier infrastructure to do so. All total, pumping in maximum D-T fuel can produce about 31 million RF/t with enough turbines.

As a further addition, this all also means the minimum injection rates for self sustaining fusion is much higher. An injection rate of 14 is required for air cooled and 26 for water cooled. So even getting things started is a fair bit more costly. All numbers above were taken at 98 injection rate.

### **Fission**

|                               | Output per 1000 mb (FE) | Rate (FE/t) |
| ----------------------------- | :---------------------: | :---------: |
| Basic Fission + Basic Turbine |        28,437,500       |   570,910   |

## **Turbine Details**

**(Credits: Telemenar)**

The following tables attempt to lay out the most efficient path to building turbines at a given size. The first aims to produce as much power as possible from incoming steam. These would be best used with Fusion or with a low burn rate Fission reactor to get the most out of them.

The second table attempts to move as much steam as possible in order to maximize the cooling going back to the source of steam. They are best used for running a hot Fission reactor in order to produce byproducts as quickly as possible, for instance in generating Anti-Matter. Of course, a good source of power will still be needed to keep the conversion of Polonium to Anti-Matter moving at a matching rate.

### **Optimized for Power Production**

| Width | Height | Casing | Structural Glass | Rotors | Coils | Dispersers | Vents | Condensers | Steam Max Flow (mB/t) | Energy Production (FE/t) |
| :---: | :----: | :----: | :--------------: | :----: | :---: | :--------: | :---: | ---------: | --------------------: | :----------------------: |
|   5   |    9   |   69   |        48        |    4   |   2   |      8     |   45  |         16 |             1,024,000 |          468,114         |
|   7   |   13   |   117  |        120       |    6   |   3   |     24     |  125  |         63 |             4,000,000 |         2,742,857        |
|   9   |   17   |   173  |        224       |    8   |   4   |     48     |  245  |        123 |             7,840,000 |         7,168,000        |
|   11  |   18   |   225  |        324       |    9   |   5   |     80     |  333  |        167 |            10,656,000 |        10,960,457        |
|   13  |   18   |   281  |        396       |    9   |   5   |     120    |  429  |        215 |            13,728,000 |        14,120,229        |
|   15  |   18   |   345  |        520       |   10   |   5   |     168    |  481  |        241 |            15,392,000 |        17,590,857        |
|   17  |   18   |   417  |        600       |   10   |   5   |     224    |  585  |        293 |            18,720,000 |        21,394,286        |

### **Optimized for Steam Recycling**

| Width | Height | Casing | Structural Glass | Rotors | Coils | Dispersers | Vents | Condensers | Steam Max Flow (mB/t) | Energy Production (FE/t) |
| :---: | :----: | :----: | :--------------: | :----: | :---: | :--------: | :---: | ---------: | --------------------: | :----------------------: |
|   5   |    9   |   69   |        48        |    4   |   2   |      8     |   45  |         16 |             1,024,000 |          468,114         |
|   7   |   13   |   117  |        60        |    3   |   2   |     24     |  185  |         93 |             4,515,840 |         1,548,288        |
|   9   |   17   |   173  |        84        |    3   |   2   |     48     |  385  |        193 |            12,320,000 |         4,224,000        |
|   11  |   18   |   225  |        108       |    3   |   2   |     80     |  549  |        275 |            17,568,000 |         6,023,314        |
|   13  |   18   |   281  |        132       |    3   |   2   |     120    |  693  |        347 |            22,176,000 |         7,603,200        |
|   15  |   18   |   345  |        104       |    2   |   1   |     168    |  897  |        449 |            28,704,000 |         6,560,914        |
|   17  |   18   |   417  |        120       |    2   |   1   |     224    |  1065 |        533 |            34,080,000 |         7,789,714        |

## **Wind and Solar**

The Wind Generator has had it's max output reduced, but the effective range of generation has been narrowed. This means that max output is achieved at y90 instead of y256. Overall, this is a buff at sea level and promotes placing them at more reasonable altitudes. Note that the y-level is calculated at the turbine of the Wind Generator.

Solar is untouched and roughly in line with wind, other than the fact it doesn't produce at night.

| Generator                | Rate (FE/t) |
| ------------------------ | :---------: |
| Wind Generator (y40)     |      24     |
| Wind Generator (y60)     |      72     |
| Wind Generator (y90)     |     120     |
| Solar Generator          |     21.8    |
| Advanced Solar Generator |    130.8    |
