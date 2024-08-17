# Compatible devices

A list of Charge Controllers and other devices that have been tested (feel free to submit a PR with ones you have tried).

:grey_question: means untested,
:white_check_mark: means tested and compatible,
:x: means tested and incompatible

## Renogy Smart Batteries
| Model               | RNGBridge V3 485   | RS485Bridge V4     | Notes |
|:--------------------|--------------------|--------------------|-------|
| `RBT100LFP12S-LFP`  | :white_check_mark: | :white_check_mark: | 12VDC 100Ah LiFePo4 |

## Renogy MPPT Charge Controllers

### Rover Series

#### Elite
| Model               | RNGBridge V3 485   | RS485Bridge V4     | Notes |
|:--------------------|--------------------|--------------------|-------|
| `RCC20RVRE-G1`      | :white_check_mark: | :white_check_mark: |20A |
| `RCC40RVRE-G1`      | :grey_question:    | :white_check_mark: |40A |

#### Li
| Model               | RNGBridge V2       | RNGBridge V3 232   | RNGBridge V3 485   | RS232Bridge V4     | RS485Bridge V4     | Notes |
|:--------------------|--------------------|--------------------|--------------------|--------------------|--------------------|-------|
| `RNG-CTRL-RVR20`    | :white_check_mark: | :white_check_mark: | :x:                | :white_check_mark: | :x:                | 20A model, aka `ROVER20A` |
| `RNG-CTRL-RVR30`    | :white_check_mark: | :white_check_mark: | :x:                | :white_check_mark: | :x:                | 30A model, aka `ROVER30A` |
| `RNG-CTRL-RVR40`    | :white_check_mark: | :white_check_mark: | :x:                | :white_check_mark: | :x:                | 40A model, aka `ROVER40A` |
| `RNG-CTRL-RVR60`    | :white_check_mark: | :white_check_mark: | :x:                | :white_check_mark: | :x:                | 60A model, aka `ROVER60A` |
| `RNG-CTRL-RVR100`   | :white_check_mark: | :white_check_mark: | :grey_question:    | :white_check_mark: | :grey_question:    | 100A model, aka `ROVER100A` |

## Renogy PWM Charge Controllers

### Wanderer
| Model               | RNGBridge V2       | RNGBridge V3 232   | RS232Bridge V4     | Notes |
|:--------------------|--------------------|--------------------|--------------------|-------|
| `RNG-CTRL-WND10`    | :white_check_mark: | :white_check_mark: | :white_check_mark: | 10A |
| `RNG-CTRL-WND30-LI` | :white_check_mark: | :white_check_mark: | :white_check_mark: | 30A |

### Adventurer
| Model               | RNGBridge V2       | RNGBridge V3 232   | RS232Bridge V4     | Notes |
|:--------------------|--------------------|--------------------|--------------------|-------|
| `RNG-CTRL-ADV30-LI` | :white_check_mark: | :white_check_mark: | :white_check_mark: | 30A |

## EPEVER Charge Controllers

### XTRA
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `XTRA1206N`         | :grey_question:    | 12/24VDC 10A |
| `XTRA2206N`         | :grey_question:    | 12/24VDC 20A |
| `XTRA1210N`         | :grey_question:    | 12/24VDC 10A |
| `XTRA2210N`         | :grey_question:    | 12/24VDC 20A |
| `XTRA3210N`         | :grey_question:    | 12/24VDC 30A |
| `XTRA4210N`         | :grey_question:    | 12/24VDC 40A |
| `XTRA3215N`         | :grey_question:    | 12/24VDC 30A |
| `XTRA4215N`         | :grey_question:    | 12/24VDC 40A |
| `XTRA3415N`         | :grey_question:    | 12/24/36/48VDC 30A |
| `XTRA4415N`         | :grey_question:    | 12/24/36/48VDC 40A |

### XTRA-N G3
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
|'XTRA1206N G3/G3 BLE'| :grey_question:    | 12/24VDC 10A |
|'XTRA2206N G3/G3 BLE'| :grey_question:    | 12/24VDC 20A |
|'XTRA1210N G3/G3 BLE'| :grey_question:    | 12/24VDC 10A |
|'XTRA2210N G3/G3 BLE'| :grey_question:    | 12/24VDC 20A |
|'XTRA3210N G3/G3 BLE'| :grey_question:    | 12/24VDC 30A |
|'XTRA4210N G3/G3 BLE'| :grey_question:    | 12/24VDC 40A |
|'XTRA3215N G3/G3 BLE'| :grey_question:    | 12/24VDC 30A |
|'XTRA4215N G3/G3 BLE'| :grey_question:    | 12/24VDC 40A |
|'XTRA3415N G3/G3 BLE'| :grey_question:    | 12/24/36/48VDC 30A |
|'XTRA4415N G3/G3 BLE'| :grey_question:    | 12/24/36/48VDC 40A |

### Tracer
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `Tracer1206AN`      | :grey_question:    | 12/24VDC 10A |
| `Tracer2206AN`      | :grey_question:    | 12/24VDC 20A |
| `Tracer1210AN`      | :grey_question:    | 12/24VDC 10A |
| `Tracer2210AN`      | :grey_question:    | 12/24VDC 20A |
| `Tracer3210AN`      | :grey_question:    | 12/24VDC 30A |
| `Tracer4210AN`      | :white_check_mark: | 12/24VDC 40A |
| `Tracer6210AN`      | :grey_question:    | 12/24VDC 60A |
| `Tracer5415AN`      | :grey_question:    | 12/24/36/48VDC 50A |
| `Tracer6415AN`      | :grey_question:    | 12/24/36/48VDC 60A |
| `Tracer8415AN`      | :grey_question:    | 12/24/36/48VDC 80A |
| `Tracer10415AN`     | :grey_question:    | 12/24/36/48VDC 100A |
| `Tracer5420AN`      | :grey_question:    | 12/24/36/48VDC 50A |
| `Tracer6420AN`      | :grey_question:    | 12/24/36/48VDC 60A |
| `Tracer8420AN`      | :grey_question:    | 12/24/36/48VDC 80A |
| `Tracer10420AN`     | :grey_question:    | 12/24/36/48VDC 100A |

### Tracer BP
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `Tracer2606BP`      | :grey_question:    | 12/24VDC 10A |
| `Tracer3906BP`      | :grey_question:    | 12/24VDC 15A |
| `Tracer5206BP`      | :grey_question:    | 12/24VDC 20A |
| `Tracer2610BP`      | :grey_question:    | 12/24VDC 10A |
| `Tracer3910BP`      | :grey_question:    | 12/24VDC 15A |
| `Tracer5210BP`      | :grey_question:    | 12/24VDC 20A |
| `Tracer7810BP`      | :grey_question:    | 12/24VDC 30A |

### Tracer BPL
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `Tracer2606BPL`     | :grey_question:    | 12/24VDC 10A |
| `Tracer3906BPL`     | :grey_question:    | 12/24VDC 15A |
| `Tracer5206BPL`     | :grey_question:    | 12/24VDC 20A |
| `Tracer2610BPL`     | :grey_question:    | 12/24VDC 10A |
| `Tracer3910BPL`     | :grey_question:    | 12/24VDC 15A |
| `Tracer5210BPL`     | :grey_question:    | 12/24VDC 20A |

### Tracer-CPN
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `Tracer5206CPN/Tracer5206CPN(BLE)`     | :grey_question:    | 12/24VDC 20A |
| `Tracer7810CPN/Tracer7810CPN(BLE)`     | :grey_question:    | 12/24VDC 30A |

### LS-B
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `LS1024B`           | :grey_question:    | 12/24VDC 10A |
| `LS2024B`           | :grey_question:    | 12/24VDC 20A |
| `LS3024B`           | :grey_question:    | 12/24VDC 30A |

### VS-BN
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `VS1024BN`          | :grey_question:    | 12/24VDC 10A |
| `VS2024BN`          | :grey_question:    | 12/24VDC 20A |
| `VS3024BN`          | :grey_question:    | 12/24VDC 30A |
| `VS4524BN`          | :grey_question:    | 12/24VDC 45A |
| `VS6024BN`          | :grey_question:    | 12/24VDC 60A |
| `VS4548BN`          | :grey_question:    | 12/24/36/48VDC 45A |
| `VS6048BN`          | :grey_question:    | 12/24/36/48VDC 60A |

### GoMate
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `GM3024N`           | :grey_question:    | 12/24VDC 30A |

### DuoRacer
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `DR1106N-DDB/DDS`   | :grey_question:    | 12VDC 10A |
| `DR2106N-DDB/DDS`   | :grey_question:    | 12VDC 20A |
| `DR3106N-DDB/DDS`   | :grey_question:    | 12VDC 30A |
| `DR1206N-DDB/DDS`   | :grey_question:    | 12/24VDC 10A |
| `DR2206N-DDB/DDS`   | :grey_question:    | 12/24VDC 20A |
| `DR3206N-DDB/DDS`   | :grey_question:    | 12/24VDC 30A |
| `DR2210N-DDB/DDS`   | :grey_question:    | 12/24VDC 20A |
| `DR3210N-DDB/DDS`   | :grey_question:    | 12/24VDC 30A |

### MSC-N
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `MSC2210N`          | :grey_question:    | 12/24VDC 20A |
| `MSC3210N`          | :grey_question:    | 12/24VDC 30A |
| `MSC4210N`          | :grey_question:    | 24VDC 40A |
| `MSC4215N`          | :grey_question:    | 24VDC 40A |

### iTracer-ND
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `IT6415ND`          | :grey_question:    | 12/24/36/48VDC 60A |

## EPEVER Inverters

### IPower
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `IP1000-11`         | :grey_question:    | 12VDC 800W 110/120VAC |
| `IP1000-12`         | :grey_question:    | 12VDC 800W 220/230VAC |
| `IP1000-21`         | :grey_question:    | 12VDC 800W 110/120VAC |
| `IP1000-22`         | :grey_question:    | 12VDC 800W 220/230VAC |
| `IP1500-11`         | :grey_question:    | 12VDC 1200W 110/120VAC |
| `IP1500-12`         | :grey_question:    | 12VDC 1200W 220/230VAC |
| `IP1500-21`         | :grey_question:    | 12VDC 1200W 110/120VAC |
| `IP1500-22`         | :grey_question:    | 12VDC 1200W 220/230VAC |
| `IP2000-21`         | :grey_question:    | 12VDC 1600W 110/120VAC |
| `IP2000-22`         | :grey_question:    | 12VDC 1600W 220/230VAC |
| `IP2000-41`         | :grey_question:    | 12VDC 1600W 110/120VAC |
| `IP2000-42`         | :grey_question:    | 12VDC 1600W 220/230VAC |

### IPower-Plus
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `IP500-11-Plus`     | :grey_question:    | 12VDC 500W 110/120VAC |
| `IP500-12-Plus`     | :grey_question:    | 12VDC 500W 220/230VAC |
| `IP500-21-Plus`     | :grey_question:    | 24VDC 500W 110/120VAC |
| `IP500-22-Plus`     | :grey_question:    | 24VDC 500W 220/230VAC |
| `IP1000-11-Plus`    | :grey_question:    | 12VDC 1000W 110/120VAC |
| `IP1000-12-Plus`    | :grey_question:    | 12VDC 1000W 220/230VAC |
| `IP1000-21-Plus`    | :grey_question:    | 24VDC 1000W 110/120VAC |
| `IP1000-22-Plus`    | :grey_question:    | 24VDC 1000W 220/230VAC |
| `IP1500-11-Plus`    | :grey_question:    | 12VDC 1500W 110/120VAC |
| `IP1500-12-Plus`    | :grey_question:    | 12VDC 1500W 220/230VAC |
| `IP1500-21-Plus`    | :grey_question:    | 24VDC 1500W 110/120VAC |
| `IP1500-22-Plus`    | :grey_question:    | 24VDC 1500W 220/230VAC |
| `IP1500-41-Plus`    | :grey_question:    | 48VDC 1500W 110/120VAC |
| `IP1500-42-Plus`    | :grey_question:    | 48VDC 1500W 220/230VAC |
| `IP2000-11-Plus`    | :grey_question:    | 12VDC 2000W 110/120VAC |
| `IP2000-12-Plus`    | :grey_question:    | 12VDC 2000W 220/230VAC |
| `IP2000-21-Plus`    | :grey_question:    | 24VDC 2000W 110/120VAC |
| `IP2000-22-Plus`    | :grey_question:    | 24VDC 2000W 220/230VAC |
| `IP2000-41-Plus`    | :grey_question:    | 48VDC 2000W 110/120VAC |
| `IP2000-42-Plus`    | :grey_question:    | 48VDC 2000W 220/230VAC |
| `IP3000-11-Plus`    | :grey_question:    | 12VDC 3000W 110/120VAC |
| `IP3000-12-Plus`    | :grey_question:    | 12VDC 3000W 220/230VAC |
| `IP3000-21-Plus`    | :grey_question:    | 24VDC 3000W 110/120VAC |
| `IP3000-22-Plus`    | :grey_question:    | 24VDC 3000W 220/230VAC |
| `IP3000-41-Plus`    | :grey_question:    | 48VDC 3000W 110/120VAC |
| `IP3000-42-Plus`    | :grey_question:    | 48VDC 3000W 220/230VAC |
| `IP4000-41-Plus`    | :grey_question:    | 48VDC 4000W 110/120VAC |
| `IP4000-42-Plus`    | :grey_question:    | 48VDC 4000W 220/230VAC |
| `IP5000-42-Plus`    | :grey_question:    | 48VDC 5000W 220/230VAC |

### NPower
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `NP600-11`          | :grey_question:    | 12VDC 600W 110/120VAC |
| `NP1000-11`         | :grey_question:    | 12VDC 1000W 110/120VAC |
| `NP1000-21`         | :grey_question:    | 24VDC 1000W 110/120VAC |
| `NP1000-42`         | :grey_question:    | 48VDC 1000W 220/230VAC |
| `NP1200-12`         | :grey_question:    | 12VDC 1200W 220/230VAC |
| `NP1200-22`         | :grey_question:    | 24VDC 1200W 220/230VAC |
| `NP1500-12`         | :grey_question:    | 12VDC 1500W 220/230VAC |
| `NP1500-22`         | :grey_question:    | 24VDC 1500W 220/230VAC |
| `NP2000-11`         | :grey_question:    | 12VDC 2000W 110/120VAC |
| `NP2000-12`         | :grey_question:    | 12VDC 2000W 220/230VAC |
| `NP2000-21`         | :grey_question:    | 24VDC 2000W 110/120VAC |
| `NP2000-22`         | :grey_question:    | 24VDC 2000W 220/230VAC |
| `NP2000-41`         | :grey_question:    | 48VDC 2000W 110/120VAC |
| `NP2000-42`         | :grey_question:    | 48VDC 2000W 220/230VAC |
| `NP2500-11`         | :grey_question:    | 12VDC 2500W 110/120VAC |
| `NP2500-12`         | :grey_question:    | 12VDC 2500W 220/230VAC |
| `NP2500-21`         | :grey_question:    | 24VDC 2500W 110/120VAC |
| `NP2500-22`         | :grey_question:    | 24VDC 2500W 220/230VAC |
| `NP2500-41`         | :grey_question:    | 48VDC 2500W 110/120VAC |
| `NP2500-42`         | :grey_question:    | 48VDC 2500W 220/230VAC |
| `NP3000-22`         | :grey_question:    | 24VDC 3000W 220/230VAC |
| `NP3000-42`         | :grey_question:    | 48VDC 3000W 220/230VAC |
| `NP3500-42`         | :grey_question:    | 48VDC 3500W 220/230VAC |
| `NP4000-22`         | :grey_question:    | 24VDC 4000W 220/230VAC |
| `NP4000-42`         | :grey_question:    | 48VDC 4000W 220/230VAC |
| `NP5000-42`         | :grey_question:    | 48VDC 5000W 220/230VAC |

### IPB
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `IPB500-12`         | :grey_question:    | 12VDC 500W 220/230/240VAC |
| `IPB1000-12`        | :grey_question:    | 12VDC 1000W 220/230/240VAC |
| `IPB1500-12`        | :grey_question:    | 12VDC 1500W 220/230/240VAC |
| `IPB2000-12`        | :grey_question:    | 12VDC 2000W 220/230/240VAC |
| `IPB3000-12`        | :grey_question:    | 12VDC 3000W 220/230/240VAC |

### IPT
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `IPT350-11`         | :grey_question:    | 12VDC 350W 110/120VAC |
| `IPT350-12`         | :grey_question:    | 12VDC 350W 220/230VAC |
| `IPT350-21`         | :grey_question:    | 24VDC 350W 110/120VAC |
| `IPT350-22`         | :grey_question:    | 24VDC 350W 220/230VAC |
| `IPT500-11`         | :grey_question:    | 12VDC 500W 110/120VAC |
| `IPT500-12`         | :grey_question:    | 12VDC 500W 220/230VAC |
| `IPT500-21`         | :grey_question:    | 24VDC 500W 110/120VAC |
| `IPT500-22`         | :grey_question:    | 24VDC 500W 220/230VAC |
| `IPT1000-11`        | :grey_question:    | 12VDC 1000W 110/120VAC |
| `IPT1000-12`        | :grey_question:    | 12VDC 1000W 220/230VAC |
| `IPT1000-21`        | :grey_question:    | 24VDC 1000W 110/120VAC |
| `IPT1000-22`        | :grey_question:    | 24VDC 1000W 220/230VAC |
| `IPT1500-11`        | :grey_question:    | 12VDC 1500W 110/120VAC |
| `IPT1500-12`        | :grey_question:    | 12VDC 1500W 220/230VAC |
| `IPT1500-21`        | :grey_question:    | 24VDC 1500W 110/120VAC |
| `IPT1500-22`        | :grey_question:    | 24VDC 1500W 220/230VAC |
| `IPT1500-41`        | :grey_question:    | 48VDC 1500W 110/120VAC |
| `IPT1500-42`        | :grey_question:    | 48VDC 1500W 220/230VAC |
| `IPT2000-11`        | :grey_question:    | 12VDC 2000W 110/120VAC |
| `IPT2000-12`        | :grey_question:    | 12VDC 2000W 220/230VAC |
| `IPT2000-21`        | :grey_question:    | 24VDC 2000W 110/120VAC |
| `IPT2000-22`        | :grey_question:    | 24VDC 2000W 220/230VAC |
| `IPT2000-41`        | :grey_question:    | 48VDC 2000W 110/120VAC |
| `IPT2000-42`        | :grey_question:    | 48VDC 2000W 220/230VAC |
| `IPT3000-11`        | :grey_question:    | 12VDC 3000W 110/120VAC |
| `IPT3000-12`        | :grey_question:    | 12VDC 3000W 220/230VAC |
| `IPT3000-21`        | :grey_question:    | 24VDC 3000W 110/120VAC |
| `IPT3000-22`        | :grey_question:    | 24VDC 3000W 220/230VAC |
| `IPT3000-41`        | :grey_question:    | 48VDC 3000W 110/120VAC |
| `IPT3000-42`        | :grey_question:    | 48VDC 3000W 220/230VAC |
| `IPT4000-41`        | :grey_question:    | 48VDC 4000W 110/120VAC |
| `IPT4000-42`        | :grey_question:    | 48VDC 4000W 220/230VAC |
| `IPT5000-42`        | :grey_question:    | 48VDC 5000W 220/230VAC |

## EPEVER Inverter/Charger

### Upower
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `UP1000-M3212`      | :grey_question:    | 12VDC 800W 220/230VAC |
| `UP1000-M3222`      | :grey_question:    | 24VDC 800W 220/230VAC |
| `UP1500-M3222`      | :grey_question:    | 24VDC 1200W 220/230VAC |
| `UP2000-M3322`      | :grey_question:    | 24VDC 1600W 220/230VAC |
| `UP3000-M3322`      | :grey_question:    | 24VDC 2400W 220/230VAC |
| `UP3000-M6322`      | :grey_question:    | 24VDC 2400W 220/230VAC |

### Upower-HI
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `UP2000-HM6021`     | :grey_question:    | 24VDC 2000W 110/120VAC |
| `UP2000-HM6022`     | :grey_question:    | 24VDC 2000W 220/230VAC |
| `UP3000-HM10021`    | :grey_question:    | 24VDC 3000W 110/120VAC |
| `UP3000-HM10022`    | :grey_question:    | 24VDC 3000W 220/230VAC |
| `UP3000-HM5041`     | :grey_question:    | 48VDC 3000W 110/120VAC |
| `UP3000-HM5042`     | :grey_question:    | 48VDC 3000W 220/230VAC |
| `UP3000-HM8041`     | :grey_question:    | 48VDC 3000W 110/120VAC |
| `UP5000-HM8042`     | :grey_question:    | 48VDC 5000W 220/230VAC |

### HP
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `HP3522-AH1250P20SA`| :grey_question:    | 24VDC 3500W 220/230VAC |
| `HP3522-AH1250P30A` | :grey_question:    | 24VDC 3500W 220/230VAC |
| `HP3522-AH1250P65A` | :grey_question:    | 24VDC 3500W 220/230VAC |
| `HP3542-AH0650P20SA`| :grey_question:    | 48VDC 3500W 220/230VAC |
| `HP3542-AH0650P30A` | :grey_question:    | 48VDC 3500W 220/230VAC |
| `HP3542-AH0650P65A` | :grey_question:    | 48VDC 3500W 220/230VAC |
| `HP5542-AH1050P20SA`| :grey_question:    | 48VDC 5500W 220/230VAC |
| `HP5542-AH1050P30A` | :grey_question:    | 48VDC 5500W 220/230VAC |
| `HP5542-AH1050P65A` | :grey_question:    | 48VDC 5500W 220/230VAC |

### UC
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `UC3522-1250P20/C`  | :grey_question:    | 24VDC 3500W 220/230VAC |
| `UC3542-0650P20/C`  | :grey_question:    | 48VDC 3500W 220/230VAC |
| `UC5542-1050P20/C`  | :grey_question:    | 48VDC 5500W 220/230VAC |

### KR
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `KR3522-1250P20/C`  | :grey_question:    | 24VDC 3500W 220/230VAC |
| `KR3542-0650P20/C`  | :grey_question:    | 48VDC 3500W 220/230VAC |
| `KR5542-1050P20/C`  | :grey_question:    | 48VDC 5500W 220/230VAC |

### KP
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
|`KP3542-AH0650P20PS/C`| :grey_question:   | 48VDC 3500W 220/230VAC |
|`KP3542-AH0650P20NS/C`| :grey_question:   | 48VDC 3500W 220/230VAC |
|`KP5542-AH1050P20PD/C`| :grey_question:   | 48VDC 5500W 220/230VAC |
|`KP5542-AH1050P20ND/C`| :grey_question:   | 48VDC 5500W 220/230VAC |
|`KP5542-AH1050P20PS/C`| :grey_question:   | 48VDC 5500W 220/230VAC |
|`KP5542-AH1050P20NS/C`| :grey_question:   | 48VDC 5500W 220/230VAC |

## EPEVER ESS

### HPS-AL
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `HPS1022-AL0210`    | :grey_question:    | 1000W 220VAC |
| `HPS1522-AL0210`    | :grey_question:    | 1500W 220VAC |
| `HPS2522-AL0315`    | :grey_question:    | 2500W 220VAC |

### HPS-AHL
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `HPS1022-AHL0210`   | :grey_question:    | 1000W 220VAC |
| `HPS1522-AHL0310`   | :grey_question:    | 1500W 220VAC |
| `HPS2522-AHL0610`   | :grey_question:    | 2500W 220VAC |

### ROH-H-P20
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `ROH5542H-05X1P20`  | :grey_question:    | 5.12KWH 5500W 220/230VAC |
| `ROH5542H-10X2P20`  | :grey_question:    | 10.24KWH 5500W 220/230VAC |
| `ROH5542H-15X3P20`  | :grey_question:    | 15.36KWH 5500W 220/230VAC |
| `ROH5542H-20X4P20`  | :grey_question:    | 20.48KWH 5500W 220/230VAC |
| `ROH5542H-25X5P20`  | :grey_question:    | 25.6KWH 5500W 220/230VAC |
| `ROH5542H-30X6P20`  | :grey_question:    | 30.72KWH 5500W 220/230VAC |

### ROH-F-P20
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `ROH5542F-05X1P20`  | :grey_question:    | 5.12KWH 5500W 220/230VAC |
| `ROH5542F-10X2P20`  | :grey_question:    | 10.24KWH 5500W 220/230VAC |
| `ROH5542F-15X3P20`  | :grey_question:    | 15.36KWH 5500W 220/230VAC |
| `ROH5542F-20X4P20`  | :grey_question:    | 20.48KWH 5500W 220/230VAC |
| `ROH5542F-25X5P20`  | :grey_question:    | 25.6KWH 5500W 220/230VAC |
| `ROH5542F-30X6P20`  | :grey_question:    | 30.72KWH 5500W 220/230VAC |

### ROH-F-P30
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
| `ROH5542F-05X1P30`  | :grey_question:    | 5.12KWH 5500W 220/230VAC |
| `ROH5542F-10X2P30`  | :grey_question:    | 10.24KWH 5500W 220/230VAC |
| `ROH5542F-15X3P30`  | :grey_question:    | 15.36KWH 5500W 220/230VAC |
| `ROH5542F-20X4P30`  | :grey_question:    | 20.48KWH 5500W 220/230VAC |
| `ROH5542F-25X5P30`  | :grey_question:    | 25.6KWH 5500W 220/230VAC |
| `ROH5542F-30X6P30`  | :grey_question:    | 30.72KWH 5500W 220/230VAC |

### Powercube 2.0 Storage Cabinet
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
|`Powercube-M-NBN-P25`| :grey_question:    | 89kWh-125kWh 25kW 220/230VAC |
| `Powercube-NBN-P50` | :grey_question:    | 143kWh-215kWh 50kW 220/230VAC |
| `Powercube-NBN-P100`| :grey_question:    | 215kWh 100kW 220/230VAC |

## EPEVER Battery
| Model               | RS485Bridge V4     | Notes |
|:--------------------|--------------------|-------|
|`LFP5.12KWH51.2V-P20R1`| :grey_question:  | 51.2VDC 100Ah LiFeP04 |


## RICH SOLAR Charge Controllers
| Model               | RNGBridge V2       | RNGBridge V3 232   | RNGBridge V3 485   | RS232Bridge V4     | RS485Bridge V4     | Notes |
|:--------------------|--------------------|--------------------|--------------------|--------------------|--------------------|-------|
| `RS-MPPT20`         | :white_check_mark: | :white_check_mark: | :x:                | :white_check_mark: | :x:                | 20A |
| `RS-MPPT30`         | :grey_question:    | :grey_question:    | :x:                | :grey_question:    | :x:                | 30A |
| `RS-MPPT40`         | :grey_question:    | :grey_question:    | :x:                | :grey_question:    | :x:                | 40A |
| `RS-MPPT60`         | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | 60A |

## SRNE Charge Controllers
| Model               | RNGBridge V2       | RNGBridge V3 232   | RNGBridge V3 485   | RS232Bridge V4     | RS485Bridge V4     | Notes |
|:--------------------|--------------------|--------------------|--------------------|--------------------|--------------------|-------|
| `MT2410`            | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | 10A 12/24VDC |
| `ML2420/ML2420-C`   | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | 20A 12/24VDC |
| `ML2430/ML2430-C`   | :white_check_mark: | :white_check_mark: | :grey_question:    | :white_check_mark: | :grey_question:    | 30A 12/24VDC |
| `ML2440/ML2440-C`   | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | 40A 12/24VDC |
| `ML4830N15`         | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | 30A 12/24/36/48VDC |
| `ML4860N15`         | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | 60A 12/24/36/48VDC |
| `LC2430N10H`        | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 30A 12/24VDC |
| `MF48100N50`        | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 100A 48VDC |
| `MC4860N15`         | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 60A 12/24/36/48VDC |
| `MC4870N15`         | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 70A 12/24/36/48VDC |
| `MC4885N15`         | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 85A 12/24/36/48VDC |
| `MC48100N15`        | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 100A 12/24/36/48VDC |
| `MC4860N25`         | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 60A 12/24/36/48VDC |
| `MC4870N25`         | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 70A 12/24/36/48VDC |
| `MC4885N25`         | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 85A 12/24/36/48VDC |
| `MC48100N25`        | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 100A 12/24/36/48VDC |
| `MA2430N15`         | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 30A 12/24VDC |
| `MA2440N15`         | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 40A 12/24VDC |
| `MA2460N15`         | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 60A 12/24VDC |
| `MA4830N15`         | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 30A 12/24/36/48VDC |
| `Shiner2410`        | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 10A 12/24VDC |
| `Shiner2420`        | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 20A 12/24VDC |
| `Shiner2430`        | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 30A 12/24VDC |
| `Shiner2440`        | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 40A 12/24VDC |
| `Shiner2460`        | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 60A 12/24VDC |
| `Shiner4820`        | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 20A 12/24/36/48VDC |

## TOYO Charge Controllers
| Model               | RNGBridge V2       | RNGBridge V3 232   | RNGBridge V3 485   | RS232Bridge V4     | RS485Bridge V4     | Notes |
|:--------------------|--------------------|--------------------|--------------------|--------------------|--------------------|-------|
| `ML2420`            | :white_check_mark: | :white_check_mark: | :grey_question:    | :white_check_mark: | :grey_question:    | 20A, 12/24VDC |
| `ML2440`            | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | 40A, 12/24VDC |
| `ML2430`            | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | 30A, 12/24VDC |
| `ML4860`            | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | 60A, 12/24/36/48VDC |
