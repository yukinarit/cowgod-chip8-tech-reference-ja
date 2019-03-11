# 2.1 メモリ

Chip-8は0x000(0)から0xFFF(4095)の4KB (4,096バイト)のRAMを持つ。最初の512バイト0x000から0x1FFはインタプリタ自身が使う領域なのでプログラマでは使用してはならない。

ほとんどのChip-8用プログラムは0x200(512)から、いくつかの実装は0x600(1536)から始まる。0x600(1536)始まるプログラムはETI660用である。

```
Memory Map:
+---------------+= 0xFFF (4095) End of Chip-8 RAM
|               |
|               |
|               |
|               |
|               |
| 0x200 to 0xFFF|
|     Chip-8    |
| Program / Data|
|     Space     |
|               |
|               |
|               |
+- - - - - - - -+= 0x600 (1536) Start of ETI 660 Chip-8 programs
|               |
|               |
|               |
+---------------+= 0x200 (512) Start of most Chip-8 programs
| 0x000 to 0x1FF|
| Reserved for  |
|  interpreter  |
+---------------+= 0x000 (0) Start of Chip-8 RAM
```
