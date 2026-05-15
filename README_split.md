# ESPHome Configuration Split

The original `v0.98.yaml` file has been split into multiple smaller YAML files organized in the `packages/` subfolder.

## Structure

- `main.yaml`: Main configuration file that includes all packages
- `packages/core.yaml`: ESP32, logger, WiFi, captive portal, OTA, web server
- `packages/globals.yaml`: All global variables
- `packages/mqtt.yaml`: MQTT configuration and text sensors for MQTT settings
- `packages/switches.yaml`: Switch components
- `packages/scripts.yaml`: Script definitions
- `packages/canbus.yaml`: CAN bus configuration and on_frame handlers
- `packages/sensors.yaml`: All sensor definitions (text and numeric)
- `packages/numbers.yaml`: All number input components
- `packages/buttons.yaml`: All button components
- `packages/intervals.yaml`: All interval definitions

## Usage

To use the split configuration:

1. Use `main.yaml` as your primary ESPHome configuration file
2. The packages are automatically included and merged
3. All functionality remains identical to the original `v0.98.yaml`

## Verification

The configuration has been structured according to ESPHome's package system, which merges YAML files at the top level. This maintains all the original functionality while improving maintainability and organization.

To compile, run:
```bash
esphome compile main.yaml
```

The split configuration should compile successfully as it preserves the exact same structure and content as the original file.