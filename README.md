# Zephyr XIAO RP2040 Blinky

A simple LED blinky application for the Seeed XIAO RP2040 board running Zephyr RTOS.

## Building
```bash
(zephyrproject) zephyr-xiao-rp2040-blinky $ cat ~/setup_zephyr.sh
```

```bash
#!/bin/bash
# save as ~/setup_zephyr.sh

# Activate virtual environment
source ~/zephyrproject/.venv/bin/activate

# Set environment variables
export ZEPHYR_BASE=~/zephyrproject/zephyr
export ZEPHYR_SDK_INSTALL_DIR=~/zephyr-sdk-0.17.2

# Source Zephyr environment
source ~/zephyrproject/zephyr/zephyr-env.sh

echo "Zephyr environment ready!"
echo "ZEPHYR_BASE: $ZEPHYR_BASE"
echo "SDK: $ZEPHYR_SDK_INSTALL_DIR"
```


```bash
# Set up Zephyr environment
source ~/setup_zephyr.sh

# Build the project
west build -b xiao_rp2040
```

Plug the XIAO-RP2040 into the computer while holding the `B` button.

```bash
# Flash to device
west flash
```

## Features

- Blinks the onboard LED every second
- Logs status messages via USB CDC ACM console
- Uses Zephyr's GPIO API and device tree
