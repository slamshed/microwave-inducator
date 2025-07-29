# Microwave Indicator Light Blueprint
This Home Assistant blueprint turns on a red light while the microwave is running and a green light for 60 seconds after it finishes.

## Features

- Red traffic light shows when microwave is actively cooking
- Green ytaffic light turns on after cooking finishes
- Automatically switches from red to green
- Fully customisable: power sensor, entities, thresholds, and timing

## Requirements

- A power sensor that reports in watts (IKEA smart plug)
- Two smart shelly switches on lights (for red and green traffic lights)
- Home Assistant with automation and blueprint support

## Import This Blueprint

Use the following URL in Home Assistant → Settings → Blueprints → Import Blueprint:

https://github.com/slamshedE/microwave-indicator-blueprint/blob/main/_
