---
cover: ../../.gitbook/assets/Enigmatica_6_1900x400.png
coverY: 0
---

# Powah

## Developer Notes

We've nerfed Powah's passive enery generation while buffing Reactor energy generation quite a bit in order to make them more appealing.

We implemented these changes in this Pull Request: https://github.com/NillerMedDild/Enigmatica6/pull/1248

The Starter tier of every machine has been removed.

Most recipes are now direct crafts, rather than tiered crafts, greatly reducing the cost of various generators. This goes hand in hand with an overall reduction in output of the more passive generators, such as solar.

An upgrade path still exists, allowing the player to take an old generator and insert new components into it, bringing it up to a higher tier. Any tier can be changed to any other tier.

{% hint style="info" %}
The following values represent Normal mode only. Expert mode increases many of these even further.
{% endhint %}

## Thermo Generators

Heat Sources have seen an overall reduction in efficiency while a new coolant has been introduced that's better than water.

In terms of RF generation, the low end has been boosted while the high end has been nerfed as shown below.

### Water Cooled

| Tier                  | Lava | Magma | Blazing Block | Nitro Block | Extraction Cap (FE/t) |
| --------------------- | ---- | ----- | ------------- | ----------- | --------------------- |
| Thermo Gen (Basic)    | 130  | 156   | 182           | 286         | 2419                  |
| Thermo Gen (Hardened) | 140  | 168   | 196           | 308         | 2739                  |
| Thermo Gen (Blazing)  | 150  | 180   | 210           | 330         | 3059                  |
| Thermo Gen (Niotic)   | 160  | 192   | 224           | 352         | 3379                  |
| Thermo Gen (Spirited) | 170  | 204   | 238           | 374         | 3699                  |
| Thermo Gen (Nitro)    | 180  | 216   | 252           | 396         | 4019                  |

### Liquid Starlight Cooled

| Tier                  | Lava | Magma | Blazing Block | Nitro Block | Extraction Cap (FE/t) |
| --------------------- | ---- | ----- | ------------- | ----------- | --------------------- |
| Thermo Gen (Hardened) | 796  | 956   | 1354          | 1752        | 2739                  |
| Thermo Gen (Blazing)  | 853  | 1024  | 1450          | 1877        | 3059                  |
| Thermo Gen (Niotic)   | 910  | 1092  | 1547          | 2002        | 3379                  |
| Thermo Gen (Spirited) | 967  | 1160  | 1644          | 2127        | 3699                  |
| Thermo Gen (Nitro)    | 1024 | 1229  | 1740          | 2252        | 4019                  |

### I-C Honey Cooled

| Tier                  | Lava | Magma | Blazing Block | Nitro Block | Extraction Cap (FE/t) |
| --------------------- | ---- | ----- | ------------- | ----------- | --------------------- |
| Thermo Gen (Basic)    | 1319 | 1583  | 1847          | 2902        | 2419                  |
| Thermo Gen (Hardened) | 1420 | 1705  | 1989          | 3125        | 2739                  |
| Thermo Gen (Blazing)  | 1522 | 1826  | 2131          | 3348        | 3059                  |
| Thermo Gen (Niotic)   | 1623 | 1948  | 2273          | 3571        | 3379                  |
| Thermo Gen (Spirited) | 1725 | 2070  | 2415          | 3795        | 3699                  |
| Thermo Gen (Nitro)    | 1826 | 2192  | 2557          | 4018        | 4019                  |

## Solar Panels

Due to the simplicity of running Solar, these are being brought a little lower. Like Thermo, the low end has been raised to make the entry level more useful, while the top tier has been reduced.

| Tier     | Rate (FE/t) |
| -------- | ----------- |
| Basic    | 220         |
| Hardened | 320         |
| Blazing  | 420         |
| Niotic   | 520         |
| Spirited | 620         |
| Nitro    | 720         |

## Magmators and Furnators

No changes. These can be considered burst power sources as a single piece of fuel is always worth the same amount of energy. Higher tiers simply burn it faster with no efficiency gains or losses.

## Reactors

These have been given a 50% boost in overall production value. The inclusion of better coolants also allows them to run much more efficiently, stretching fuel even further. Do note that these values are approximate as Powah Reactors naturally fluctuate over time, largely depending on how much fuel is left in the tank. Maximum output is achieved only when the tank is full (1000mb). A single piece of fuel is worth 100mb, so the generation rate will fluctuate as the tank goes up and down between 900 and 1000. These numbers assume the use of Redstone, Carbon, and Dry Ice to augment the reactor.

### Water Cooled

| Tier     | Output Per Fuel (FE) | Burn Rate (mb/t) | Temp | Generation Rate (FE/t) |
| -------- | -------------------- | ---------------- | ---- | ---------------------- |
| Basic    | 34,843,750           | 0.0249           | 29   | 9,385.50               |
| Hardened | 61,093,750           | 0.0298           | 29   | 19,709.54              |
| Blazing  | 74,843,750           | 0.0348           | 29   | 28,156.49              |
| Niotic   | 147,343,750          | 0.0398           | 29   | 63,352.09              |
| Spirited | 184,375,000          | 0.0448           | 29   | 89,162.20              |
| Nitro    | 235,781,250          | 0.0497           | 29   | 126,704.18             |

### I-C Honey Cooled

| Tier     | Output Per Fuel (FE) | Burn Rate (mb/t) | Temp | Generation Rate (FE/t) |
| -------- | -------------------- | ---------------- | ---- | ---------------------- |
| Basic    | 46,250,000           | 0.0189           | 22   | 9,431.48               |
| Hardened | 80,937,500           | 0.0226           | 22   | 19,806.11              |
| Blazing  | 99,062,500           | 0.0264           | 22   | 28,294.44              |
| Niotic   | 195,156,250          | 0.0302           | 22   | 63,662.48              |
| Spirited | 244,218,750          | 0.034            | 22   | 89,599.05              |
| Nitro    | 312,343,750          | 0.0377           | 22   | 127,324.97             |

### Ether Gas Cooled

| Tier     | Output Per Fuel (FE) | Burn Rate (mb/t) | Temp | Generation Rate (FE/t) |
| -------- | -------------------- | ---------------- | ---- | ---------------------- |
| Basic    | 112,812,500          | 0.0077           | 9    | 9,516.88               |
| Hardened | 199,687,500          | 0.0093           | 9    | 19,985.44              |
| Blazing  | 244,531,250          | 0.0108           | 9    | 28,550.63              |
| Niotic   | 481,562,500          | 0.0123           | 9    | 64,238.92              |
| Spirited | 602,500,000          | 0.0139           | 9    | 90,410.34              |
| Nitro    | 770,625,000          | 0.0154           | 9    | 128,477.85             |
