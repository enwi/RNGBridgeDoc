# Tested Controllers

A list of Renogy Charge Controllers that have been tested (feel free to submit a PR with ones you have tried).

:grey_question: means untested,
:white_check_mark: means tested and compatible,
:x: means tested and incompatible

## MPPT Charge Controllers

### Rover Series

#### Elite
| Model               | Version | RNGBridge V2       | RNGBridge V3 232   | RNGBridge V3 485   | Notes |
|:--------------------|---------|--------------------|--------------------|--------------------|-------|
| `RCC20RVRE-G1`      | VXXXXXX | :x:                | :x:                | :white_check_mark: | 20A model |
| `RCC40RVRE-G1`      | VXXXXXX | :x:                | :x:                | :grey_question:    | 40A model |

#### Li
| Model               | Version | RNGBridge V2       | RNGBridge V3 232   | RNGBridge V3 485   | Notes |
|:--------------------|---------|--------------------|--------------------|--------------------|-------|
| `RNG-CTRL-RVR20`    | V030001 | :white_check_mark: | :white_check_mark: | :grey_question:    | 20A model, aka `ROVER20A` |
| `RNG-CTRL-RVR30`    | VXXXXXX | :grey_question:    | :grey_question:    | :grey_question:    | 30A model, aka `ROVER30A` |
| `RNG-CTRL-RVR40`    | V030001 | :white_check_mark: | :white_check_mark: | :grey_question:    | 40A model, aka `ROVER40A` |
| `RNG-CTRL-RVR60`    | VXXXXXX | :white_check_mark: | :white_check_mark: | :grey_question:    | 60A model, aka `ROVER60A` |
| `RNG-CTRL-RVR100`   | VXXXXXX | :grey_question:    | :grey_question:    | :grey_question:    | 100A model, aka `ROVER100A` |

## PWM Charge Controllers

### Wanderer
| Model               | Version | RNGBridge V2       | RNGBridge V3 232   | RNGBridge V3 485   | Notes |
|:--------------------|---------|--------------------|--------------------|--------------------|-------|
| `RNG-CTRL-WND10`    | VXXXXXX | :white_check_mark: | :white_check_mark: | :grey_question:    | 10A model |
| `RNG-CTRL-WND30-LI` | VXXXXXX | :grey_question:    | :grey_question:    | :grey_question:    | 30A model |

### Voyager (waterproof)
| Model               | Version | RNGBridge V2       | RNGBridge V3 232   | RNGBridge V3 485   | Notes |
|:--------------------|---------|--------------------|--------------------|--------------------|-------|
| `RCC10VOYP-G1`      | VXXXXXX | :grey_question:    | :grey_question:    | :grey_question:    | 10A model |
| `RCC20VOYP-G1 `     | VXXXXXX | :grey_question:    | :grey_question:    | :grey_question:    | 20A model |

### Adventurer
| Model               | Version | RNGBridge V2       | RNGBridge V3 232   | RNGBridge V3 485   | Notes |
|:--------------------|---------|--------------------|--------------------|--------------------|-------|
| `RNG-CTRL-ADV30-LI` | VXXXXXX | :grey_question:    | :grey_question:    | :grey_question:    | 30A model |

## Non Renogy models

### RICH SOLAR
| Model               | Version | RNGBridge V2       | RNGBridge V3 232   | RNGBridge V3 485   | Notes |
|:--------------------|---------|--------------------|--------------------|--------------------|-------|
| `20 Amp MPPT`       | VXXXXXX | :white_check_mark: | :white_check_mark: | :grey_question:    | 20A model |
| `40 Amp MPPT`       | VXXXXXX | :grey_question:    | :grey_question:    | :grey_question:    | 40A model |

### SRNE
| Model               | Version | RNGBridge V2       | RNGBridge V3 232   | RNGBridge V3 485   | Notes |
|:--------------------|---------|--------------------|--------------------|--------------------|-------|
| `SR-MT2410`         | VXXXXXX | :grey_question:    | :grey_question:    | :grey_question:    | 10A model |
| `SR-ML2420`         | VXXXXXX | :grey_question:    | :grey_question:    | :grey_question:    | 20A model |
| `SR-ML2430`         | VXXXXXX | :white_check_mark: | :white_check_mark: | :grey_question:    | 30A model |
| `SR-ML4860`         | VXXXXXX | :grey_question:    | :grey_question:    | :grey_question:    | 60A model |

### TOYO
| Model               | Version | RNGBridge V2       | RNGBridge V3 232   | RNGBridge V3 485   | Notes |
|:--------------------|---------|--------------------|--------------------|--------------------|-------|
| `SR-ML2420`         | VXXXXXX | :white_check_mark: | :white_check_mark: | :grey_question:    | 20A, 12/24V |
| `SR-ML2440`         | VXXXXXX | :grey_question:    | :grey_question:    | :grey_question:    | 40A, 12/24V |
| `SR-ML2430`         | VXXXXXX | :grey_question:    | :grey_question:    | :grey_question:    | 30A, 12/24V |
| `SR-ML4860`         | VXXXXXX | :grey_question:    | :grey_question:    | :grey_question:    | 60A, 12/24/36/48V |
