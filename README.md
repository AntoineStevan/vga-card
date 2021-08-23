## Table Of Content.
- [1  ](https://github.com/Supaero-Computer-Science-Club/6502-game-of-GLIDER/tree/main/#1-the-hardware-toc                               ) The Hardware.
- [2  ](https://github.com/Supaero-Computer-Science-Club/6502-game-of-GLIDER/tree/main/#2-the-software-technical-details-toc             ) The software: technical details.
- [2.1](https://github.com/Supaero-Computer-Science-Club/6502-game-of-GLIDER/tree/main/#21-objects-binary-representations-toc            ) Objects binary representations.
- [2.2](https://github.com/Supaero-Computer-Science-Club/6502-game-of-GLIDER/tree/main/#22-obstacles-array-structure-toc                 ) Obstacles array sructure.
- [3  ](https://github.com/Supaero-Computer-Science-Club/6502-game-of-GLIDER/tree/main/#3-run-the-code-toc                               ) Run the code.

| ![glider-debouncer-schematics.png](https://github.com/Supaero-Computer-Science-Club/6502-game-of-GLIDER/blob/main/res/glider-debouncer-schematics.png) | 
|:--:| 
| *The Debouncer Circuit* |

## 1 The Hardware. [[toc](https://github.com/Supaero-Computer-Science-Club/6502-game-of-GLIDER/tree/main/#table-of-content)]

| component   | hsync | vsync | sub-total:sync | card | integration |  sub-total:sync+int | transceiver |  total |
|-------------|-------|-------|----------------|------|-------------|---------------------|-------------|--------|
| flip-flop   |   12  |   12  |        24      |   1  |             |          25         |             |    25  |
| not         |    9  |    5  |        14      |      |             |          14         |      49     |    63  |
| 8-NAND      |    4  |    4  |         8      |      |             |           8         |             |     8  |
| 2-NAND      |    4  |    4  |         8      |   2  |      1      |          11         |      16     |    27  |
| 2-NOR       |       |       |         0      |      |             |           0         |      18     |    18  |
| 2-AND       |       |       |         0      |      |      1      |           1         |             |     1  |
| transistor  |       |       |         0      |      |             |           0         |      32     |    32  |
| logic tot.  |   17  |   13  |        30      |   2  |      2      |          34         |     115     |   149  |
| memory tot. |   12  |   12  |        24      |   1  |      0      |          25         |       0     |    25  |
