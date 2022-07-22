Shield: [![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg

inverter-hardware (mainboard mini)
==================================
**KiCad** schematics and board for J. Huebner and openinverter.org inverter - main board mini version.

# Table of Contents
<details>
 <summary>Click to open TOC</summary>
<!-- MarkdownTOC autolink="true" levels="1,2,3,4,5,6" bracket="round" style="unordered" indent="    " autoanchor="false" markdown_preview="github" -->

- [About](#about)
    - [Changes brought by this repository](#changes-brought-by-this-repository)
- [Ecosystem](#ecosystem)
    - [Hardware](#hardware)
    - [Firmware](#firmware)
- [Regarding this board](#regarding-this-board)
    - [Usual disclaimer](#usual-disclaimer)
    - [Setup](#setup)
    - [Design](#design)
    - [Custom fields for Manufacturer Part Numbers](#custom-fields-for-manufacturer-part-numbers)
    - [Fabrication](#fabrication)

<!-- /MarkdownTOC -->
</details>

# About
This repository, "**openinverter-hw-mainboard-mini**", hosts the KiCad schematics for OpenInverter.org "mainboard mini" inverter.

It's a derivative of [inverter hardware](https://github.com/jsphuebner/inverter-hardware) by J. Huebner and openinverter.org used under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0)

[**openinverter-hw-mainboard-mini**](https://github.com/llange/openinverter-hw-mainboard-mini) &copy; 2022 by [llange](https://github.com/llange) is licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0)

It is an [Open Source Hardware](https://www.oshwa.org/definition/) project: _"Open source hardware is hardware whose design is made publicly available so that anyone can study, modify, distribute, make, and sell the design or hardware based on that design. The hardware’s source, the design from which it is made, is available in the preferred format for making modifications to it."_

As such, we publish:
* the original schematic and board layout files - to allow people modify the hardware
* alternative or intermediate formats that can be viewed or edited ([PDFs of circuit schematics](documentation/mainboard-mini\ schematic.pdf), [Gerbers for circuit board layouts](production/), ...) - to allow people to study or make some use of the design without having to use KiCad for that.

## Changes brought by this repository
According to the terms of the license, we notify you that this [**openinverter-hw-mainboard-mini**](https://github.com/llange/openinverter-hw-mainboard-mini) is a modification of the original [inverter hardware mainboard mini (schematics)](https://github.com/jsphuebner/inverter-hardware/blob/master/mainboard-mini.sch) and [inverter hardware mainboard mini (board)](https://github.com/jsphuebner/inverter-hardware/blob/master/mainboard-mini.brd) with the following changes:
* Conversion (from Eagle) to [KiCad 6.0](https://www.kicad.org/)
* Change of parts symbols and footprints to better integrate in KiCad ecosystem (esp. 3D rendering)
* Many errors have certainly been introduced in the process !!

# Ecosystem

This hardware is part of a broad ecosystem and community (OpenInverter) of enthusiasts that aims to democratize the EV conversion landscape, by researching and sharing knowledge ; and creating hardware (such as this one) to help buildings EV.

You can find more informations here:
* [OpenInverter Web site](https://openinverter.org/)
* [OpenInverter Forum](https://openinverter.org/forum/)
* [OpenInverter Wiki](https://openinverter.org/wiki/)
* [EVBMW](https://www.evbmw.com/)

Main contributors
* [Johannes Huebner](https://github.com/jsphuebner/)
* [Damien Maguire](https://github.com/damienmaguire/)
* ...and a lot of others that I forgot to put here - sorry!

## Hardware

You can buy original boards (not this one but the [original Eagle board](https://github.com/jsphuebner/inverter-hardware/blob/master/mainboard-mini.brd)):
* [OpenInverter shop - mainoard mini - community edition](https://openinverter.org/shop/index.php?route=product/product&path=59&product_id=70)
* [OpenInverter shop - BMW i3™ inverter drop-in board - community edition](https://openinverter.org/shop/index.php?route=product/product&path=59&product_id=72)
* [OpenInverter shop - Nissan Leaf™ Gen 2 controller - community edition](https://openinverter.org/shop/index.php?route=product/product&path=59&product_id=57)
* [OpenInverter shop - Nissan Leaf™ Gen 2 controller - with personal support](https://openinverter.org/shop/index.php?route=product/product&path=59&product_id=53)

## Firmware
You can find the firmware for this board [here](https://github.com/jsphuebner/stm32-sine).

# Regarding this board

![3D view](/img/mainboard-mini.jpg)
![PCB view](/img/mainboard-mini-pcb.png)

## Usual disclaimer
All files are provided as-is. Physical realization of any circuit requires design review and appropriate selection of components.  

The information provided in this repository is intended as information only. The Open Inverter project and it's contributors take no responsibility for how you use the information contained within these pages, nor any liability for damage, harm, injuries, or death, that may result from your actions.  

You undertake **your** project at **your own risk**. 

## Setup
_Please note : I (llange) don't design circuits for a living, and am by no means a KiCad expert. All design issues you'll find in this repository have certainly been accidentally intoduced by me at some point. Don't use this repository without your own judgment and experience._  

To properly use this repository you will need:
* A working [KiCad installation (>= 6.x)](https://www.kicad.org/)
* The [Fabrication Toolkit for KiCad](https://github.com/bennymeg/JLC-Plugin-for-KiCad) (JLC PCB Plug-in for KiCad) if you want to order make your boards with JLCPCB

Of course there are other possible plugins to enable you to automate the making of your boards with other providers, here are some examples among the many available:
* [PCBWay Plug-in for Kicad](https://github.com/pcbway/PCBWay-Plug-in-for-Kicad)
* [NextPCB Plug-in for Kicad](https://gitlab.com/nextpcbofficial/NextPCB-Plug-in-for-Kicad/)
* [AISLER Push for KiCad](https://github.com/AislerHQ/PushForKiCad)
* [kicad-gerberzipper](https://github.com/g200kg/kicad-gerberzipper)
* [KiKit – Automation for KiCAD](https://github.com/yaqwsx/KiKit)
* etc ...

## Design
* I try to have all ERC / DRC warnings and errors removed.
* In the future I'll try to add specific constraints for manufacturers (don't know yet what is possible with kicad_dru files)

## Custom fields for Manufacturer Part Numbers

You'll find that all these plugins expect some kind of "Part Number" reference field for each component:
* For AISLER plugin it's one of ['mpn', 'MPN', 'Mpn', 'AISLER_MPN'](https://github.com/AislerHQ/PushForKiCad/blob/2b171c85127c3b3b01a7c3be513bdc8cd8693f6d/src/push_thread.py#L171)
* For JLCPCB plugin it's one of ['mpn', 'Mpn', 'MPN', 'JLC_MPN', 'LCSC_MPN', 'LCSC Part #', 'JLC', 'LCSC'](https://github.com/bennymeg/JLC-Plugin-for-KiCad/blob/a39b65c94c322160cc0accf409dcafcb7271a910/plugins/process.py#L186)
* For PCBWay plugin it's one of ['mpn', 'MPN', 'Mpn', 'PCBWay_MPN'](https://github.com/pcbway/PCBWay-Plug-in-for-Kicad/blob/4dc1a54cb858d88d19062207046e60a83a8cbea9/plugins/thread.py#L151)
* For NextPCB plugin it's one of ['mpn', 'MPN', 'Mpn', 'NextPCB_MPN'](https://gitlab.com/nextpcbofficial/NextPCB-Plug-in-for-Kicad/-/blob/0c57b36d220ea69d5c8d31feb5939e7f558bd829/plugins/thread.py#L151)
* etc...

I'd recommend to use the most specific one ; i.e. do **not** use the fields ['mpn', 'MPN', 'Mpn'] as it's likely that the part number will be very different from one provider to the other, and we want to let the end-user choose his own manufacturer.

For JLC PCB I used the **JLC** field name. You're welcome to use **AISLER_MPN**, **PCBWay_MPN** and **NextPCB_MPN** if you use those providers, etc... 

## Fabrication
(This has not been tested yet. Please review all files / component selection before doing any fabrication process)
In theory:
* In KiCad, produce manufacturing file by clicking on the "Fabrication Toolkit" icon
* A folder (`production`) will open with some files:
  * gerber.zip : a zip containing all the 4 files below, plus the gerber files (copper traces, drilling instructions, ...) 
  * bom.csv : The Bill Of Materials - needed for purchasing parts
  * designators.csv : ?
  * netlist.ipc : IPC netlist file
  * positions.csv : Pick and Place file
* Upload this file to JLCPCB and follow the process

_(To be continued...)_
