# 🏠 Home Assistant Blueprints

A collection of Home Assistant automation blueprints by [@joohann](https://github.com/joohann).

## Blueprints

### 🏠 Appliance Done Notification

Sends a push notification when an appliance (washing machine, dryer, dishwasher, etc.) has finished its cycle. Uses power consumption data to detect when the appliance is truly done, with protection against false alerts from short power dips.

**Features:**
- Configurable power threshold and stability duration
- Skips notification if appliance was never truly active
- Supports multiple notification devices
- Works with any power sensor

[![Import blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2Fjoohann%2Fha-blueprints%2Fmain%2Fblueprints%2Fautomation%2Fappliance-done-notification.yaml)

---

### 🚨 National Siren Test Notification

Sends a critical push notification 30 seconds before the monthly national siren test. Triggers on the first Monday of the month, suppressed on public holidays.

**Features:**
- Configurable trigger time
- Public holiday calendar check
- Critical push notification (bypasses silent mode)
- Supports multiple notification devices
- Suitable for the Netherlands (WAS-Alert) and similar countries

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
    └── national-siren-test-notification.yaml
```

## License

MIT License — feel free to use, modify, and share.
