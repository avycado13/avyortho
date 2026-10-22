# AvyOrtho
A basic 40% ortholinear keyboard that uses vim keys for arrows

![PCB](https://cdn.hackclub.com/01a0a7b5-c42a-7a9b-b89f-9c23be1c408a/avyortho-3a.png)
![CAD of case](https://cdn.hackclub.com/01a0ac86-9aba-7f96-a21d-458dd03c107e/avyortho-4.png)

I wanted to make a nice keyboard and I wanted one that could be small and easy to carry in my backpack. I decided on an ortholinear because I figured they would be a lot easier to build and route because the keys aren't spaced weirdly. I decided to use ZMK for my firmware because there are nice tools to let you export your JSON from keyboard layout editor and turn it into firmware for ZMK. I used a Seeed Studios XIAO nRF52840 Plus for the microcontroller because it had enough GPIO pins and because it could do batteries without external devices needed

 I chose to go with a minimal 4x12 setup so I could fit it in my bag and to make it cooler. I will probably do keys like function keys with a layer and a modifier key for other functionality. In my next keyboard, I might consider adding RGB lights with something like a sk6812-mini. I will probably mainly use this keyboard on the go and then build a bigger keyboard as my home keyboard.

## Bill of Materials

PCB components (designators and footprints in [`production/bom.csv`](production/bom.csv)). Prices below are USD snapshots from the selected offers in [`ordering/`](ordering/), **not live quotes**; check price, stock, shipping, and tax before ordering.

| Part | Qty on PCB | Order qty | Part / supplier link | Unit price | Order cost |
|------|-----------:|----------:|----------------------|-----------:|-----------:|
| 1N4148W SMD diodes (D1–D48, except D44) | 47 | 50 | [LCSC C241939](https://lcsc.com/product-detail/C241939.html) | $0.037 | $1.85 |
| 806 kΩ 0805 resistor (R1) | 1 | 1 | [Vishay CRCW0805806KFKEA — Mouser 71-CRCW0805-806K-E3](https://www.mouser.com/ProductDetail/71-CRCW0805-806K-E3) | $0.10 | $0.10 |
| 2 MΩ 0805 resistor (R2) | 1 | 1 | [TE CPF0805B2M0E — Mouser 279-CPF0805B2M0E](https://www.mouser.com/ProductDetail/279-CPF0805B2M0E) | $0.25 | $0.25 |
| Kailh MX hotswap sockets (SW1–SW48, except SW44) | 47 | 3 × 20-pack | [Adafruit 4958](https://www.adafruit.com/product/4958) ([Mouser 485-4958](https://www.mouser.com/ProductDetail/485-4958)) | $4.95 / pack | $14.85 |
| Seeed XIAO nRF52840 Plus (U3) | 1 | 1 | [Mouser 713-102010672](https://www.mouser.com/ProductDetail/713-102010672) | $10.40 | $10.40 |
| **PCB component total** | | | | | **$27.45** |

R2's selected offer is an alternative to the BOM's CRCW08052M00FKED (same 2 MΩ value and 0805 size); confirm specifications before substituting. The sockets are priced per **20-pack**, not individually. The total excludes shipping, tax, PCB fabrication, and the following build-dependent items (no specific product or price selected):

- 47 × MX-compatible switches — choose a compatible switch and check its current price.
- 47 × 1u MX-compatible keycaps — choose a set and check its current price.
- Case and plate — see the [case CAD](cad/body.step) and [plate CAD](cad/plate.step) for fabrication; cost depends on material and manufacturer.
