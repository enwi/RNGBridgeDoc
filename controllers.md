# Compatible devices

A list of Charge Controllers and other devices that have been tested (feel free to submit a PR with ones you have tried).

:grey_question: means untested,
:white_check_mark: means tested and compatible,
:x: means tested and incompatible

## Renogy Smart Batteries
| Model               | RNGBridge V3 485   | RS485Bridge V4     | Notes |
|:--------------------|--------------------|--------------------|-------|
| `RBT100LFP12S-LFP`  | :white_check_mark: | :white_check_mark: | 12V 100Ah LiFePo4 |

## Renogy MPPT Charge Controllers

### Rover Series

#### Elite
| Model               | RNGBridge V3 485   | RS485Bridge V4     | Notes |
|:--------------------|--------------------|--------------------|-------|
| `RCC20RVRE-G1`      | :white_check_mark: | :white_check_mark: |20A model |
| `RCC40RVRE-G1`      | :grey_question:    | :white_check_mark: |40A model |

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
| `RNG-CTRL-WND10`    | :white_check_mark: | :white_check_mark: | :white_check_mark: | 10A model |
| `RNG-CTRL-WND30-LI` | :white_check_mark: | :white_check_mark: | :white_check_mark: | 30A model |

### Adventurer
| Model               | RNGBridge V2       | RNGBridge V3 232   | RS232Bridge V4     | Notes |
|:--------------------|--------------------|--------------------|--------------------|-------|
| `RNG-CTRL-ADV30-LI` | :white_check_mark: | :white_check_mark: | :white_check_mark: | 30A model |

## Non Renogy models

### RICH SOLAR
| Model               | RNGBridge V2       | RNGBridge V3 232   | RNGBridge V3 485   | RS232Bridge V4     | RS485Bridge V4     | Notes |
|:--------------------|--------------------|--------------------|--------------------|--------------------|--------------------|-------|
| `RS-MPPT20`         | :white_check_mark: | :white_check_mark: | :x:                | :white_check_mark: | :x:                | 20A model |
| `RS-MPPT30`         | :grey_question:    | :grey_question:    | :x:                | :grey_question:    | :x:                | 30A model |
| `RS-MPPT40`         | :grey_question:    | :grey_question:    | :x:                | :grey_question:    | :x:                | 40A model |
| `RS-MPPT60`         | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | 60A model |

### SRNE
| Model               | RNGBridge V2       | RNGBridge V3 232   | RNGBridge V3 485   | RS232Bridge V4     | RS485Bridge V4     | Notes |
|:--------------------|--------------------|--------------------|--------------------|--------------------|--------------------|-------|
| `MT2410`            | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | 10A 12/24V model |
| `ML2420/ML2420-C`   | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | 20A 12/24V model |
| `ML2430/ML2430-C`   | :white_check_mark: | :white_check_mark: | :grey_question:    | :white_check_mark: | :grey_question:    | 30A 12/24V model |
| `ML2440/ML2440-C`   | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | 40A 12/24V model |
| `ML4830N15`         | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | 30A 12/24/36/48V model |
| `ML4860N15`         | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | 60A 12/24/36/48V model |
| `LC2430N10H`        | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 30A 12/24V model |
| `MF48100N50`        | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 100A 48V model |
| `MC4860N15`         | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 60A 12/24/36/48V model |
| `MC4870N15`         | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 70A 12/24/36/48V model |
| `MC4885N15`         | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 85A 12/24/36/48V model |
| `MC48100N15`        | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 100A 12/24/36/48V model |
| `MC4860N25`         | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 60A 12/24/36/48V model |
| `MC4870N25`         | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 70A 12/24/36/48V model |
| `MC4885N25`         | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 85A 12/24/36/48V model |
| `MC48100N25`        | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 100A 12/24/36/48V model |
| `MA2430N15`         | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 30A 12/24V model |
| `MA2440N15`         | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 40A 12/24V model |
| `MA2460N15`         | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 60A 12/24V model |
| `MA4830N15`         | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 30A 12/24/36/48V model |
| `Shiner2410`        | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 10A 12/24V model |
| `Shiner2420`        | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 20A 12/24V model |
| `Shiner2430`        | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 30A 12/24V model |
| `Shiner2440`        | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 40A 12/24V model |
| `Shiner2460`        | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 60A 12/24V model |
| `Shiner4820`        | :x:                | :x:                | :grey_question:    | :x:                | :grey_question:    | 20A 12/24/36/48V model |

### TOYO
| Model               | RNGBridge V2       | RNGBridge V3 232   | RNGBridge V3 485   | RS232Bridge V4     | RS485Bridge V4     | Notes |
|:--------------------|--------------------|--------------------|--------------------|--------------------|--------------------|-------|
| `ML2420`            | :white_check_mark: | :white_check_mark: | :grey_question:    | :white_check_mark: | :grey_question:    | 20A, 12/24V |
| `ML2440`            | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | 40A, 12/24V |
| `ML2430`            | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | 30A, 12/24V |
| `ML4860`            | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | :grey_question:    | 60A, 12/24/36/48V |
