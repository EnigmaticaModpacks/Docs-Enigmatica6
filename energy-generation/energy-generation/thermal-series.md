---
cover: ../../.gitbook/assets/Enigmatica_6_1900x400.png
coverY: 0
---

# Thermal Series

## Developer Notes

Some of Thermal Expansion's Dynamos have been given a significant boost in terms of FE generation. They are the slow burn, high efficiency generators of the pack.

## Dynamos

### Stirling Dynamo

The entry level dynamo, this burns any furnace fuel. To keep it in line with other furnace type generators, no changes have been made to it's output.

### Magmatic Dynamo

Another entry level dynamo, this one consumes lava to produce energy. Like the Stirling Dynamo, it's output remains default to avoid power loops.

### Compression Dynamo

Capable of burning most liquid fuels in the pack, the Compression Dynamo is a mid tier dynamo. It has been given a 10x modifier over defaults and compatibility has been added for many more fuels at varying rates.

### Lapidary Dynamo

Lapidary Dynamos have had their total output increased by 40x over default values. A number of extra fuels have also been added, allowing you to get some extra power from many of the gems that you'll find while mining.

### Numismatic Dynamo

Metals are first converted to coins in a Multi-Servo Press and then fed into the Numismatic Dynamo to produce energy. Like the Lapidary Dynamo, this has been given a 40x multiplier on output FE.

#### Rates

Exact values for all fuels may be obtained from JEI. Simply look at 'Uses' for each dynamo to find a suitable fuel. The number shown here is the total FE generated per unit of fuel at 100% efficiency.

## Augments and Integral Components

Thermal Expansion's Dynamos use a system of replaceable upgrades to augment their capacity. There are three relevant upgrades for Dynamos:

1. Integral Components, which act as a straight multiplier to most other attributes
2. Auxiliary Reaction Chambers, which increase the FE/t rate at the cost of fuel efficiency
3. Multi-cycle Injectors, which allow the dynamo to run more efficiently

Only one Integral Component may be used at a time, but the other two may be inserted in any configuration.

As the internal buffer is filled, the dynamo will produce less FE/t, however it will not stop unless disabled by redstone. So they will always 'leak' a little energy if left running. To avoid this waste, it is recommended to send the power into a battery of some sort (`$storage/energy` to see your options in JEI) and then use a comparator and simple redstone circuits to disable the generators when the battery is nearly full.

The Values below assume a Diamond as fuel in a Lapidary Dynamo, though the math should be straight forward for any other fuel type. All dynamos work the same.

### Base (100% Efficiency)

| Integral Components | Minimum FE/t Produced | Max FE/t Produced | Total FE Produced |
| ------------------- | :-------------------: | :---------------: | :---------------: |
| None                |           4           |         40        |     20,000,000    |
| Hardened            |           8           |         80        |     20,000,000    |
| Reinforced          |           12          |        120        |     20,000,000    |
| Resonant            |           16          |        160        |     20,000,000    |

### 3x Auxiliary Reaction Chambers (73% Efficiency)

| Integral Components | Minimum FE/t Produced | Max FE/t Produced | Total FE Produced |
| ------------------- | :-------------------: | :---------------: | :---------------: |
| None                |           16          |        160        |     14,600,000    |
| Hardened            |           32          |        320        |     14,600,000    |
| Reinforced          |           48          |        480        |     14,600,000    |
| Resonant            |           64          |        640        |     14,600,000    |

### 3x Multi-Cycle Injectors (133% Efficiency)

| Integral Components | Minimum FE/t Produced | Max FE/t Produced | Total FE Produced |
| ------------------- | :-------------------: | :---------------: | :---------------: |
| None                |           4           |         40        |     26,600,000    |
| Hardened            |           8           |         80        |     26,600,000    |
| Reinforced          |           12          |        120        |     26,600,000    |
| Resonant            |           16          |        160        |     26,600,000    |
