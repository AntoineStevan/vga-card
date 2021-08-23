# Simple VGA card.
This project is greatly based on the VGA "world's worst video card" from Ben Eater's Youtube channel.  
One can find more information in his dedicated video series and [here](https://eater.net/vga).

## Table Of Content.
- [1](https://github.com/AntoineStevan/vga-card/tree/main/#1-schematics-toc ) Schematics.
- [2](https://github.com/AntoineStevan/vga-card/tree/main/#2-datasheets-toc ) Datasheets.
- [3](https://github.com/AntoineStevan/vga-card/tree/main/#3-part-counts-toc) Part counts.

## 1 Schematics. [[toc](https://github.com/AntoineStevan/vga-card/tree/main/#table-of-content)]
| ![hsync.png](https://github.com/AntoineStevan/vga-card/blob/main/res/hsync.png) | 
|:--:| 
| *The hsync Circuit* |

| ![vsync.png](https://github.com/AntoineStevan/vga-card/blob/main/res/vsync.png) | 
|:--:| 
| *The vsync Circuit* |

| ![card.png](https://github.com/AntoineStevan/vga-card/blob/main/res/card.png) | 
|:--:| 
| *The complete Card* |

## 2 Datasheets. [[toc](https://github.com/AntoineStevan/vga-card/tree/main/#table-of-content)]
MM74HCT245 Octal 3-STATE Transceiver: [here](https://www.jameco.com/Jameco/Products/ProdDS/45031.pdf)


## 3 Part Counts. [[toc](https://github.com/AntoineStevan/vga-card/tree/main/#table-of-content)]
| component   | hsync | vsync | sub-total:sync | card | integration |  sub-total:sync+int | transceiver |  total |
|-------------|-------|-------|----------------|------|-------------|---------------------|-------------|--------|
| flip-flop   |   12  |   12  |        24      |   1  |             |          25         |             |    25  |
| not         |    9  |    5  |        14      |      |             |          14         |      49     |    63  |
| 8-NAND      |    4  |    4  |         8      |      |             |           8         |             |     8  |
| 2-NAND      |    4  |    4  |         8      |   2  |      1      |          11         |      16     |    27  |
| 2-NOR       |       |       |         0      |      |             |           0         |      18     |    18  |
| 2-AND       |       |       |         0      |      |      1      |           1         |             |     1  |
| transistor  |       |       |         0      |      |             |           0         |      32     |    32  |
| memory tot. |   12  |   12  |        24      |   1  |      0      |          25         |       0     |    25  |
| logic tot.  |   17  |   13  |        30      |   2  |      2      |          34         |     115     |   149  |
