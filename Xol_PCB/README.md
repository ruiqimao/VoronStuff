# Xol PCB

![Render](Images/Render.png)
![Front](Images/Front.png)
![Back](Images/Back.png)

This is a PCB made for Armchair Engineering's [Xol Toolhead](https://github.com/Armchair-Engineering/Xol-Toolhead), featuring:
* One hotend cooling fan JST-XH connectors
* Two part cooling  fan JST-XH connectors
* One heater Micro-Fit connector
* One thermistor Micro-Fit connector
* One Neopixel JST-XH connector
* Two auxiliary JST-XH connectors
* One extruder motor connector
* Selectable fan voltage (5V, Alt, 24V)
* Integrated mount for carriage screw

## BOM

In addition to the PCB, the following connectors are needed:

| Part | Quantity | Link |
|:-:|:-:|:-:|
| Molex Micro-Fit 3.0 430451600 | 1 | [DigiKey](https://www.digikey.com/en/products/detail/molex/0430451600/531424) |
| Molex Micro-Fit 3.0 430650200 | 2 | [DigiKey](https://www.digikey.com/en/products/detail/molex/0436500200/268989) |
| JST B2B-XH-A | 4 | [DigiKey](https://www.digikey.com/en/products/detail/jst-sales-america-inc./B2B-XH-A(LF)(SN)/1651045) |
| JST B3B-XH-A | 2 | [DigiKey](https://www.digikey.com/en/products/detail/jst-sales-america-inc./B3B-XH-A/1651046) |
| JST B4B-XH-A | 1 | [DigiKey](https://www.digikey.com/en/products/detail/jst-sales-america-inc./B4B-XH-A(LF)(SN)/1651047) |

## Pinout

From the point of view looking directly at the **wiring harness connector**:

![Pinout](Images/Pinout.png)

| Pin | Usage | Pin | Usage |
|:-:|:-:|:-:|:-:|
| 1 | Neopixel | 9 | Hotend voltage |
| 2 | Part cooling fan ground | 10 | Hotend ground |
| 3 | Hotend fan ground | 11 | Alt voltage |
| 4 | Thermistor ground | 12 | Thermistor |
| 5 | Motor A1 | 13 | Motor B1 |
| 6 | Motor A2 | 14 | Motor B2 |
| 7 | Ground | 15 | Auxilary 1 |
| 8 | 5V | 16 | Auxiliary 2 |

## Selectable fan voltage

There are two sets of solder jumpers, one for each type of fan, that should be bridged to select the fan voltage.

## Extruder compatibility
The PCB and strain relief are designed with only the [Sherpa Mini](https://github.com/Annex-Engineering/Sherpa_Mini-Extruder) in mind. **Usage with other extruders may require the motor connector to be swapped to the back side.**

## Distribution board
Xol PCB is compatible with the [Xol distribution board](https://store.annex.engineering/collections/pcbs/products/carabiner-distribution-board-for-xol-toolhead) from Annex Engineering. See additional documentation [here](https://github.com/Annex-Engineering/Carabiner-Docs/tree/main/carabiner-distributor_xol).

### Alternatives
* A second Xol PCB can be used as a distribution board.
* The [Carabiner distribution board](https://github.com/Annex-Engineering/Carabiner-Docs/tree/main/carabiner-distributor) can be used as labeled with the following changes:

  | Distribution PCB | Xol PCB |
  |:-:|:-:|
  | ThChamb | RGB |
  | A1| GND |
  | A2 | AUX1 |
  | A3 | AUX2 |
  | A4 | 5V |

  Additional documentation [here](https://github.com/Annex-Engineering/Carabiner-Docs/tree/main/carabiner-distributor).

## Wiring harness

Xol PCB is compatible with the [Carabiner wiring harness](https://store.annex.engineering/products/carabiner-wiring-harness) from Annex Engineering. The long version is 1200mm, which may not sufficient for some printers.

| Printer | Compatible with Carabiner Harness |
|:-:|:-:|
| Trident 250mm | Yes |
| Trident 300mm | Yes |
| Trident 350mm | Likely (untested) |
| V2.4 250mm | Yes |
| V2.4 300mm | Yes with horizontal Z chain |
| V2.4 350mm | Unlikely (untested) |

### Alternatives

* **(Recommended)** Custom length Carabiner harness from [Annex Engineering](https://store.annex.engineering/collections/pcbs/products/carabiner-wiring-harness-custom-length-kit)
* **(Recommended)** 2.2 meter alternative from [Raven Mech](https://www.ravenmech.com/products/carabiner-pinned-cable-harness)
* Repin a 14+2 Stealthburner wiring harness (e.g. [14-pin](https://www.fabreeko.com/products/ldo-v2-4-or-trident-ptfe-toolhead-cable-1-9m-350mm-sized-build?variant=43114275537151) + [2-pin](https://kb-3d.com/store/printer-specific-harnesses/474-linneo-led-extension-harness-voron-stealth-burner-1642910819052.html) + [2x Molex Micro-Fit 3.0 0430251600](https://www.digikey.com/en/products/detail/molex/0430251600/531406?utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=PMax%20Supplier_Focus%20Supplier&utm_term=&utm_content=&gclid=EAIaIQobChMIsoGBzZrzgAMVJzmtBh1heQdKEAQYASABEgKG5PD_BwE))

## Beacon compatibility

The two AUX pins can be used for Beacon D- and D+ lines with some caveats:
* It is an untested use case
* There will be no more AUX pins left for endstop or filament sensors
* The traces are routed over ground plane splits
* 5V must be supplied from VBUS, meaning any fans running off of 5V will be powered by VBUS
* Only compatible with Annex harness, which has a twisted wire pair for D- and D+

## Purchasing

Xol PCB can currently be purchased from:

* :us: [X.R. Bunker](https://xrbunker.works/products/xol-toolhead-board-ruiqimao)
* :us: [Fabreeko](https://www.fabreeko.com/products/xol-toolhead-board-by-ruiqimao)
* :us: [West3D](https://west3d.com/products/xol-toolhead-pcb)
* :us: [Annex Engineering](https://store.annex.engineering/products/xol-toolhead-pcb)
* :canada: [NorthPrint3D](https://northprint3d.ca/product/xol-toolhead-toolboard-pcb)
* :uk: [JB3D](https://jb3d.uk/product/xol-toolhead-pcb-by-ruiqimao)
* :eu: [Lab4450](https://lab4450.com/product/xol-toolhead-board)
