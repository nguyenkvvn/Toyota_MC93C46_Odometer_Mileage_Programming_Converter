# Toyota_MC93C46_Odometer_Mileage_Programming_Converter
A small calculator and converter to assist with programming late 90s to early 00s Toyota odometers.

# Description
This is a small Excel spreadsheet I made to aid with odometer correction. The original sheet from [speedkar9](https://www.toyotanation.com/threads/diy-odometer-reprogramming.782562/) was lost to time (as it seems there is a paywall on a certain document scalper site), so I recreat it to help those who may come after me, with some additional features.

# Usage
> ⚠ WARNING: USE AT YOUR OWN RISK. NO WARRANTY OR GUARANTEE EXPRESSED OR IMPLIED. COMPLY WITH ALL APPLICABLE LAWS AND REGULATIONS FOR YOUR GIVEN LOCALITY.						

- Inputs go into yellow cells. 
- To convert from decimal to inverted hex, in the ordering Toyota proscribes in the MC93C46 chip, type in the mileage in the yellow cell in A11.
- To convert from inverted hex, as read from the MC93C46 chip, type in the value of each niblet at its respective address location.

# What you will need
- [AsProgrammer-dregmod](https://github.com/therealdreg/asprogrammer-dregmod/releases) v3.17 by therealdreg
- [CH341A EPPROM BIOS Programmer](https://amzn.to/4nxkcXT) (Amazon affiliate link)
    - This comes with an alligator clip and some pre-made pins. Everything you need is in this kit.

# Wiring Diagram to connect a 25xxxx series programmer to a 93xxxx series chip

To connect the programmer listed above, to interface with a 93xxxx series chip, you will need to pin the following from the programmer, to the breakout board, to female end of the alligator clip's ribbon cable. 

| 25xxxx | 93xxxx |
|--------|--------|
| 1 | 1 |
| 2 | 4 |
| 3 | INOP |
| 4 | 5 & 6 |
| 5 | 3 |
| 6 | 2 |
| 7 | INOP |
| 8 | 8 |

It is imperative to ensure you have perfect alignment and connection to the chip when connecting the aligator clip. It tends to be misaligned and short out, especially if it touches the board.

# Appreciation and Recognitions
- Thank you to Zevin B. from the Toyota Crown Owners (USA) Facebook group for his generous assistance with providing me a wiring diagram and a tutorial on how to reprogram a MC93C46.
- Thank you to speedkar9 from ToyotaNation.com, as I referenced his DIY guide to verify the numbers I used to test this sheet, and the original layout of his conversion sheet.