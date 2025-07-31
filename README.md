# Zephyr XIAO RP2040 Blinky

A simple LED blinky application for the Seeed XIAO RP2040 board running Zephyr RTOS.

## Building

```bash
# Set up Zephyr environment
source ~/setup_zephyr.sh

# Build the project
west build -b xiao_rp2040

# Flash to device
west flash
```

## Features

- Blinks the onboard LED every second
- Logs status messages via USB CDC ACM console
- Uses Zephyr's GPIO API and device tree
