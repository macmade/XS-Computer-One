XS Computer One - Apple 1 Replica Project
=========================================

About
-----

This project is an attempt to build a working replica of the [Apple-1] computer, made in 1976 by Steve Wozniak and released by Apple Computer Company, now Apple, Inc.

Only about 200 units of this computer were made. Today, only about 60 units still exists, and less than 10 are known working.  
They are sometimes sold at auctions, for record prices. In 2012, one was sold for $671,000.

To my knowledge, three replica projects exists:  
[Replica-1] by Vince Briel, [Mimeo-1] by Mike Willegal, and Obtronix by Steve Gabaly.

The last two are exact replicas, while the first one uses actual components with a different motherboard layout.

So this project will be (hopefully) a fourth one.

I decided to build my own replica from scratch, as it's a very nice occasion to learn about electronics.  
As a programmer, I sometimes feel frustrated not to know more about this... ; )

[Apple-1]:   http://en.wikipedia.org/wiki/Apple_I
[Replica-1]: http://www.brielcomputers.com/wordpress/?cat=17
[Mimeo-1]:   http://www.willegal.net/appleii/apple1.htm

### Roadmap

There's of course no real roadmap yet, as I'm currently learning as I go. The project will surely takes a huge amount of time, so don't expect results too soon.

Here are the actual project parts:

| # | Part                     | Status      | Description                                                                              |
|---|--------------------------|-------------|------------------------------------------------------------------------------------------|
| 1 | Learn                    | In progress | Learn as much as possible on electronics, as I'm completely new to this.                 |
| 2 | Test                     |             | Experiment with a few basic PCB and components.                                          |
| 3 | Component Identification | In progress | Get the original component specification from the original schematics and documentation. |
| 4 | Component Purchase       | In progress | Purchase components or find alternatives if they are not available anymore.              |
| 5 | ROM                      |             | Find a way to get the original ROM and have it built somehow.                            |
| 6 | Prototype                |             | Get a prototype working on a breadboard.                                                 |
| 7 | PCB Design               |             | Design the final PCB, as close as possible to the original Apple-1, and have it printed. |
| 8 | Mounting                 |             | Mount all components on the motherboard.                                                 |

Tools & Equipment
-----------------

| Manufacturer  | Part No.   | Details                      | Alternative | Quantity | Found | Status |
|---------------|------------|------------------------------|-------------|----------|-------|--------|
| B&K Precision | [DP 21]    | Logic Probe / 20 MHz - 30 Ns | N/A         | 1        | Yes   | -      |
| Fluke         | [87-V]     | True RMS Digital Multimeter  | N/A         | 1        | Yes   | -      |
|               |            | (Soldering Station)          | N/A         | 1        | No    | -      |
|               |            | (Desolder Pump)              | N/A         | 1        | No    | -      |
|               |            | (Solder)                     | N/A         | 1        | No    | -      |
|               |            | (Breadboard)                 | N/A         | 1        | No    | -      |
|               |            | (Power Transformer)          | N/A         | 1        | No    | -      |
|               |            | (Safety Glasses)             | N/A         | 1        | No    | -      |

***Note:*** *Any equivalent tool may be used. Tools listed here are the one I'll use for the project.*

[DP 21]: http://ch.mouser.com/Search/ProductDetail.aspx?R=DP_21virtualkey61500000virtualkey615-DP-21
[87-V]:  http://ch.mouser.com/ProductDetail/Fluke/FLUKE-87-V/?qs=sGAEpiMZZMuBVu7Wy0UTy5lFkCyOv5Wu

Hardware Parts - Power Supply
-----------------------------

### Power Transformers

| Manufacturer | Part No.   | Details                 | Alternative             | Quantity | Found | Status |
|--------------|------------|-------------------------|-------------------------|----------|-------|--------|
| Stancor      | [P-8380]   | 117 V / 10 V CT - 3.0 A | Triad Magnetics [F-31X] | 1        | Yes   | -      |
| Stancor      | [P-8667]   | 117 V / 28 V CT - 1.0 A | Triad Magnetics [F40X]  | 1        | Yes   | -      |


[P-8380]: https://ch.mouser.com/Search/ProductDetail.aspx?R=P-8380virtualkey53800000virtualkey802-P-8380
[P-8667]: https://ch.mouser.com/Search/ProductDetail.aspx?R=P-8667virtualkey53800000virtualkey802-P-8667
[F-31X]:  https://ch.mouser.com/Search/ProductDetail.aspx?R=F-31Xvirtualkey55310000virtualkey553-F-31X
[F40X]:   https://ch.mouser.com/Search/ProductDetail.aspx?R=F40Xvirtualkey55310000virtualkey553-F40X

### Rectifiers

| Manufacturer            | Part No. | Details                 | Alternative    | Quantity | Found | Status |
|-------------------------|----------|-------------------------|----------------|----------|-------|--------|
| ???                     | MR500    | 50 V / 3.0 A            | MCC [FR301-TP] | 4        | Yes   | -      |
| Fairchild Semiconductor | [1N4001] | 50 V / 1.0 A            | N/A            | 4        | Yes   | -      |


[FR301-TP]: https://ch.mouser.com/Search/ProductDetail.aspx?R=FR301-TPvirtualkey54720000virtualkey833-FR301-TP
[1N4001]:   https://ch.mouser.com/Search/ProductDetail.aspx?R=1N4001virtualkey51210000virtualkey512-1N4001

### Capacitors

| Manufacturer | Part No.         | Details                                       | Alternative               | Quantity | Found | Status |
|--------------|------------------|-----------------------------------------------|---------------------------|----------|-------|--------|
| Sprague      | 53D113G025JP6    | Radial Aluminum Electrolytic / 15 V - 5300 uF | ???                       | 1        | No    | -      |
| Sprague      | 53D382G050JL6    | Radial Aluminum Electrolytic / 25 V - 2400 uF | ???                       | 2        | No    | -      |
| Vishay       | [MAL213826229E3] | Radial Aluminum Electrolytic / 25 V -   22 uF | Nichicon [TVX1E220MAD1LS] | 5        | Yes   | -      |


[MAL213826229E3]: https://ch.mouser.com/Search/ProductDetail.aspx?R=MAL213826229E3virtualkey59420000virtualkey594-2222-138-26229
[TVX1E220MAD1LS]: https://ch.mouser.com/Search/ProductDetail.aspx?R=TVX1E220MAD1LSvirtualkey64700000virtualkey647-TVX1E220MAD1LS

### Voltage Regulators

| Manufacturer           | Part No.         | Details                  | Alternative                        | Quantity | Found | Status |
|------------------------|------------------|--------------------------|------------------------------------|----------|-------|--------|
| STMicroelectronics     | [LM323K]         | +15 V /  +5 V - 3.0 A    | N/A                                | 1        | Yes   | -      |
| National Semiconductor | LM320 MP-5       | -15 V /  -5 V - 1.0 A    | Fairchild Semiconductor [LM7905CT] | 1        | Yes   | -      |
| National Semiconductor | LM320 MP-12      | -25 V / -12 V - 1.0 A    | Fairchild Semiconductor [LM7912CT] | 1        | Yes   | -      |
| National Semiconductor | LM340-12         | +25 V / +12 V - 1.0 A    | Fairchild Semiconductor [LM7812CT] | 1        | Yes   | -      |

[LM323K]:   https://ch.mouser.com/Search/ProductDetail.aspx?R=LM323Kvirtualkey51120000virtualkey511-LM323K
[LM7905CT]: https://ch.mouser.com/Search/ProductDetail.aspx?R=LM7905CTvirtualkey51210000virtualkey512-LM7905CT
[LM7912CT]: https://ch.mouser.com/Search/ProductDetail.aspx?R=LM7912CTvirtualkey51210000virtualkey512-LM7912CT
[LM7812CT]: https://ch.mouser.com/Search/ProductDetail.aspx?R=LM7812CTvirtualkey51210000virtualkey512-LM7812CT

### Heatsinks

| Manufacturer | Part No.   | Details | Alternative   | Quantity | Found | Status |
|--------------|------------|---------|---------------|----------|-------|--------|
| Wakefield    | [680-125A] | 1.5 C/W | N/A           | 1        | Yes   | -      |

[680-125A]: https://ch.mouser.com/Search/ProductDetail.aspx?R=680-125Avirtualkey56720000virtualkey567-680-125A

### Fuses

| Manufacturer | Part No.      | Details                                   | Alternative   | Quantity | Found | Status |
|--------------|---------------|-------------------------------------------|---------------|----------|-------|--------|
| Littelfuse   |               | Axial Glass / 3AG Slo-Blo / 125 V - 0.5 A | ???           | 1        | No    | -      |

### Connectors

| Manufacturer | Part No.      | Details               | Alternative   | Quantity | Found | Status |
|--------------|---------------|-----------------------|---------------|----------|-------|--------|
| Molex        | [171813-0006] | 6-Pin Power Connector | N/A           | 1        | Yes   | -      |
| ???          | ???           | 4-Pin Video Connector | ???           | 1        | No    | -      |
| ???          | ???           | 22-Pin Connector      | ???           | 1        | No    | -      |
| ???          | ???           | B4 (Keyboard?)        | ???           | 1        | No    | -      |

[171813-0006]: https://ch.mouser.com/Search/ProductDetail.aspx?R=171813-0006virtualkey53810000virtualkey538-171813-0006

Hardware Parts - Terminal Section
---------------------------------

### Crystal

| Manufacturer | Part No.       | Details                | Alternative   | Quantity | Found | Status |
|--------------|----------------|------------------------|---------------|----------|-------|--------|
| ECS          | [ECS-143-S-1X] | HC-49/U / 14.31818 MHz | N/A           | 1        | Yes   | -      |

[ECS-143-S-1X]: https://ch.mouser.com/Search/ProductDetail.aspx?R=ECS-143-S-1Xvirtualkey59070000virtualkey520-HCA1431-SX

### ...

Hardware Parts - Processor Section
----------------------------------

### Processor

| Manufacturer   | Part No. | Details | Alternative   | Quantity | Found | Status |
|----------------|----------|---------|---------------|----------|-------|--------|
| MOS Technology | 6502     |         | ???           | 1        | No    | -      |

### Memory

| Manufacturer | Part No. | Details | Alternative   | Quantity | Found | Status |
|--------------|----------|---------|---------------|----------|-------|--------|
| ???          | MK4096   |         | ???           | 16       | No    | -      |

### PIA

| Manufacturer | Part No. | Details                      | Alternative   | Quantity | Found | Status |
|--------------|----------|------------------------------|---------------|----------|-------|--------|
| Motorola     | MC6820CL | Peripheral Interface Adapter | ???           | 1        | Yes   | -      |

### ...

Repository Infos
----------------

    Owner:			Jean-David Gadina - XS-Labs
    Web:			www.xs-labs.com
    Blog:			www.noxeos.com
    Twitter:		@macmade
    GitHub:			github.com/macmade
    LinkedIn:		ch.linkedin.com/in/macmade/
    StackOverflow:	stackoverflow.com/users/182676/macmade
