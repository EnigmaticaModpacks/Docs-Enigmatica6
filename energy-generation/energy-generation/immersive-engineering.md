---
cover: ../../.gitbook/assets/Enigmatica_6_1900x400.png
coverY: 0
---

# Immersive Engineering

## **Developer Notes**

Immersive Engineering's Power remains largely unchanged at this time and serve as cheap entry level power options.

## **Windmills**

Consisting of a Kinetic Dynamo and a Windmill blade, the Windmill will output 11 FE/t at any y-level. This can be enhanced by right clicking Windmill Sails onto the blades. Each sail increases output by 3 FE/t resulting in a max of 35 FE/t. These are a cheap and aesthetic entry level power supply.

## **Water Wheels**

Kinetic Dynamos also serve as the base for Water Wheels which can generate a clean 25 rf/t if. Three Water Wheels may be attached to a single dynamo in a line.

## **Diesel Generator**

The Diesel Generator will burn any of the various 'Diesel' fuels in the pack. They all generate the same amount of energy, clocking in at 498,337 FE per bucket. This burns very quickly, however, at a rate of 4096 FE/t, making this a potent generator that can last well into mid game.

Even though the fuel is burned rather inefficiently, the entire infrastructure to produce bio-diesel costs relatively little to run, resulting in a nice net positive energy production.

For example, A single Industrial Squeezer and Industrial Fermenter pair can produce enough Plant Oil and Ethanol to run a Refinery. Each Refinery is then capable of comfortably supplying bio-diesel to two generators. These ratios are not exact, so keep that in mind when scaling up.

With this infrastructure, the generators run at a comfortable 6,832 FE/t. This, or course, goes down if FE is used to generate the crops used in the process.

Note: The Diesel Generators are not 'smart' and will burn continuously even if there is nowhere to store the energy. To avoid this waste, it is recommended to send the power into a battery of some sort (`$storage/energy` to see your options in JEI) and then use a comparator and simple redstone circuits to disable the generators when the battery is nearly full.
