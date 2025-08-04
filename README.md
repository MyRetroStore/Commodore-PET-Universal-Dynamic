# Commodore PET Universal Dynamic

This is a replica PCB of the universal dynamic motherboard for the Commodore PET 

The schematics were redone in KiCad and based off the original Commodore design. 
PCB is a near-exact replica (Or as close as I could reasonable make it) to the original Commodore PCB. 


```
UNIVERSAL DYNAMIC PET
ASSY. NO. 8032089
FAB NO. 8032088
ARTWORK NO. 8032086 REV A
```

### Why create this?

After purchasing what was advertised as an 8032 PET from eBay, I discovered that the motherboard was actually a 2001 board with random ROMs inserted. Considering the absurd prices for replacement PCBs I decided it would be a fun project to design and build a Universal dynamic PET board I could use with the CRT. 

I spent several hours searching online, but no one appeared to have done a full CAD version of the schematics - and certainly no PCB layout (probably for good reason - it turned out to be a lot more work that I expected!).

The first task was recreating the schematics in KiCad. Fortunatel, the original Commodore schematics were available at [zimmers.net](https://www.zimmers.net/anonftp/pub/cbm/schematics/computers/pet/univ/), so while time consuming, it wasn't too difficult. 

The next challenge was replicating the original PCB as closely as possible - especially hard without a physical board to reference. One of the members at the [vcfed forums](https://forum.vcfed.org/index.php) kindly provided high-resolution photos of the front and back of the board. 

### Commodore Schematics

The original schematics for the Universal PET can be found here:
https://www.zimmers.net/anonftp/pub/cbm/schematics/computers/pet/univ/


### Bill of Materials
[BOM CSV](https://github.com/MyRetroStore/Commodore-PET-Universal-Dynamic/blob/main/BOM/BOM.csv)

### Hardware

The schematic and Gerber files were created in KiCad 9.

### Fixes

While tracing the original Commdore PCB and comparing it to the schematics, I came across a few design errors. These have all been corrected:

PCB:
- Removed GND VIA near UD14 pin6 - not connected
- Removed VIA to the right of R40 - not connected
- Removed GND VIA above C53 - not connected
- C37 shorted on PCB. Fixed.
- 12V test point near FB26/UD6 not labelled. Now labelled TP

Schematic:
- IEEE-488 Schematic - duplicate reference for C75. Now referenced as C98
- /EOI IN connects to J1 Pin 5, and not directly to J2 Pin 4
- J2 Pin 4 mislabelled as /EOI. Should be /EOI IN
- Cassette & Keyboard Schematic. UB2 should be labelled UB12
- UB12 Pin 8 should be /EOI, and not /EOI IN

### Testing IEEE Interface

To test the IEEE-488 bus, I would recommend reading PET and the IEEE 488 Bus by Eugene Fisher/ C.W.Jensen. 

The book includes a BASIC program for testing the port. 


### Troubleshooting

If you building or troubleshooting a PET, I highly recommend using [PETTESTER](https://forum.vcfed.org/index.php?threads/pettester-versions-and-manuals.1238265/#post-1252044) by daver2 at vcfed. 

I couldn't have built and tested this without his PETTESTER ROM- it also helped my repair a few PETs along the way (along with numerous posts and advice from daver2)




### Purchasing

If you'd like to purchase a bare PCB:
- UK buyers: Order from my [store](https://myretostore.co.uk)
- International buyers: Purchase via [eBay](https://www.ebay.co.uk/str/myretrostoreuk/Commodore/_i.html?store_cat=37608566017), with shipping through eBay's Global Shipping Program. 

### Disclaimer

This schematic and PCB design are shared in good faith and, to the best of my knowledge, are free of errors. However, I cannot guarantee their accuracy or reliability. Use them at your own risk - I accept no responsibility for any damage or malfunction from their use. 

### Copyright

All original copyrights remain with their respective owners. This project  includes elements created by others, and their rights are fully acknowledged and retained.
