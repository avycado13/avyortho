# AvyOrtho
A basic 40% ortholinear keyboard that uses vim keys for arrows

![PCB](https://cdn.hackclub.com/01a0a7b5-c42a-7a9b-b89f-9c23be1c408a/avyortho-3a.png)

I wanted to make a nice keyboard and I wanted one that could be small and easy to carry in my backpack. I decided on an ortholinear because I figured they would be a lot easier to build and route because the keys aren't spaced weirdly. I decided to use ZMK for my firmware because there are nice tools to let you export your JSON from keyboard layout editor and turn it into firmware for ZMK. I used a Seeed Studios XIAO nRF52840 Plus for the microcontroller because it had enough GPIO pins and because it could do batteries without external devices needed

 I chose to go with a minimal 4x12 setup so I could fit it in my bag and to make it cooler. I will probably do keys like function keys with a layer and a modifier key for other functionality. In my next keyboard, I might consider adding RGB lights with something like a sk6812-mini. I will probably mainly use this keyboard on the go and then build a bigger keyboard as my home keyboard.

## Bill of Materials

Components on the PCB (full BOM in [`production/bom.csv`](production/bom.csv)):

| Part | Designators | Qty | Value / Part # | Footprint | Source |
|------|-------------|-----|----------------|-----------|--------|
| Diodes | D1-D48 | 47 | 1N4148W (SMD) | D_SOD-123 | [LCSC C241939](https://lcsc.com/product-detail/C241939.html) |
| Resistor | R1 | 1 | 806kΩ | 0805 | CRCW0805806KFKEA |
| Resistor | R2 | 1 | 2MΩ | 0805 | CRCW08052M00FKED |
| MX hotswap sockets | SW1-SW48 | 47 | CPG151101S11-16 (Kailh) | SW_MX_HS | [Adafruit 4958](https://www.adafruit.com/product/4958) |
| MCU | U3 | 1 | Seeed XIAO nRF52840 Plus | XIAO-nRF52840-Plus | [Mouser 713-102010672](https://www.mouser.com/ProductDetail/713-102010672) |

Also these parts for the actual build
- 47x MX switches (any 1u, hot swappable)
- 47x keycaps (1u)
- Case + plate (see [`cad/`](cad/))
