# Random notes researching the Corsair Lighting Node Pro controller

Product: https://www.corsair.com/us/en/Categories/Products/CORSAIR-LINK/CORSAIR-Lighting-Node-PRO/p/CL-9011109-WW
Platform: Ubuntu 18.04 LTS
Configuration: 4 RGB strips, connected 2x2

Aside from the preamble already in lib/lighting_node_pro.js .. these are the bits of interest

## Initialise the first channel
Note the payload begins with `38 01 01`
```
0000   1b 00 60 1a f7 0b 04 ab ff ff 00 00 00 00 09 00
0010   00 01 00 03 00 01 01 40 00 00 00 38 01 01 00 00
0020   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
0030   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
0040   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
0050   00 00 00 00 00 00 00 00 00 00 00
```

## Set color purple (#af00ff) on first channel
Beginning with `32 00` appears to select the first channel
```
0000   1b 00 60 1a f7 0b 04 ab ff ff 00 00 00 00 09 00
0010   00 01 00 03 00 01 01 40 00 00 00 32 00 00 14 00
0020   af af af af af af af af af af af af af af af af
0030   af af af af 00 00 00 00 00 00 00 00 00 00 00 00
0040   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
0050   00 00 00 00 00 00 00 00 00 00 00

0000   1b 00 60 aa 64 0c 04 ab ff ff 00 00 00 00 09 00
0010   00 01 00 03 00 01 01 40 00 00 00 32 00 00 14 01
0020   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
0030   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
0040   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
0050   00 00 00 00 00 00 00 00 00 00 00

0000   1b 00 60 1a f7 0b 04 ab ff ff 00 00 00 00 09 00
0010   00 01 00 03 00 01 01 40 00 00 00 32 00 00 14 02
0020   ff ff ff ff ff ff ff ff ff ff ff ff ff ff ff ff
0030   ff ff ff ff 00 00 00 00 00 00 00 00 00 00 00 00
0040   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
0050   00 00 00 00 00 00 00 00 00 00 00
```

## Initialise the second channel
Note the payload begins with `38 01 02` for the second channel
```
0000   1b 00 60 1a f7 0b 04 ab ff ff 00 00 00 00 09 00
0010   00 01 00 03 00 01 01 40 00 00 00 38 01 02 00 00
0020   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
0030   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
0040   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
0050   00 00 00 00 00 00 00 00 00 00 00
```

## Set color purple(#af00ff) on second channel
Beginning with `32 01` appears to select the second channel
```
0000   1b 00 60 8a 05 08 04 ab ff ff 00 00 00 00 09 00
0010   00 01 00 03 00 01 01 40 00 00 00 32 01 00 14 00
0020   af af af af af af af af af af af af af af af af
0030   af af af af 00 00 00 00 00 00 00 00 00 00 00 00
0040   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
0050   00 00 00 00 00 00 00 00 00 00 00

0000   1b 00 90 a7 49 0c 04 ab ff ff 00 00 00 00 09 00
0010   00 01 00 03 00 01 01 40 00 00 00 32 01 00 14 01
0020   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
0030   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
0040   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
0050   00 00 00 00 00 00 00 00 00 00 00

0000   1b 00 30 78 67 0c 04 ab ff ff 00 00 00 00 09 00
0010   00 01 00 03 00 01 01 40 00 00 00 32 01 00 14 02
0020   ff ff ff ff ff ff ff ff ff ff ff ff ff ff ff ff
0030   ff ff ff ff 00 00 00 00 00 00 00 00 00 00 00 00
0040   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
0050   00 00 00 00 00 00 00 00 00 00 00
```






See also:
https://github.com/mattanger/ckb-next/wiki/CKB-Daemon-Manual
