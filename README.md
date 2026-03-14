# 🏠 Home Assistant Blueprints

A collection of Home Assistant automation blueprints by [@joohann](https://github.com/joohann).

## Blueprints

### 🪟 Curtains Based On Lux And Window State

Closes curtains automatically when lux drops below a threshold. If windows are open, waits until they are closed. The wait is aborted at sunrise (lux above open threshold AND sun above horizon). Opens curtains when it gets light again.

**Features:**
- Configurable close and open lux thresholds
- Supports multiple cover entities
- Optional window sensor check (multiple sensors supported)
- Waits for windows to close before closing curtains
- Aborts waiting at sunrise (lux high AND sun above horizon)
- Configurable delay after windows close

[![Import blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2Fjoohann%2Fha-blueprints%2Fmain%2Fblueprints%2Fautomation%2Fcurtains-lux-window.yaml)

---

### 🚽 Toilet Light - Door & Occupancy

Smart toilet lighting based on a door sensor and occupancy sensor. Light turns on when the door opens, off when it closes or when occupancy is gone. Supports day, evening, and bedtime brightness and color temperature modes.

**Features:**
- Light on when door opens, off when door closes
- Occupancy failsafe: turns off light if no occupancy detected for X seconds (open-door use)
- Day / evening / bedtime brightness and color temperature modes
- Configurable occupancy timeout

[![Import blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2Fjoohann%2Fha-blueprints%2Fmain%2Fblueprints%2Fautomation%2Ftoilet-light.yaml)

---

### 🏠 Appliance Done Notification

Sends a push notification when an appliance (washing machine, dryer, dishwasher, etc.) has finished its cycle. Uses power consumption data to detect when the appliance is truly done, with protection against false alerts from short power dips.

**Features:**
- Configurable power threshold and stability duration
- Skips notification if appliance was never truly active
- Supports multiple notification devices
- Works with any power sensor

[![Import blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2Fjoohann%2Fha-blueprints%2Fmain%2Fblueprints%2Fautomation%2Fappliance-done-notification.yaml)

---

### 🚨 Dutch Siren Test Notification

Sends a critical push notification 10 seconds before the monthly Dutch siren test (WAS-Alert). Triggers on the first Monday of the month, suppressed on public holidays.

**Features:**
- Configurable trigger time
- Public holiday calendar check
- Critical push notification on iOS and Android (bypasses silent/do not disturb)
- Supports multiple notification devices

[![Import blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2Fjoohann%2Fha-blueprints%2Fmain%2Fblueprints%2Fautomation%2Fnational-siren-test-notification.yaml)

---

## Installation

Click any **Import blueprint** button above, or import manually via:

**Settings → Automations & Scenes → Blueprints → Import Blueprint**

Paste the raw URL of the blueprint YAML file.

## Repository structure

```
blueprints/
└── automation/
    ├── appliance-done-notification.yaml
    ├── curtains-lux-window.yaml
    ├── national-siren-test-notification.yaml
    └── toilet-light.yaml
```

## License

MIT License — feel free to use, modify, and share.
