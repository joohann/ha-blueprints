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

### 🚨 Luchtalarm Test Melding

Stuurt een kritieke pushmelding 10 seconden voor de maandelijkse luchtalarmtest. Activeert op de eerste maandag van de maand, onderdrukt op feestdagen.

**Kenmerken:**
- Instelbare meldingstijd
- Feestdagenkalender controle
- Kritieke melding op iOS én Android (negeert stil/niet storen)
- Meerdere apparaten tegelijk
- Geschikt voor Nederland (WAS-Alert) en vergelijkbare landen

[![Import blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2Fjoohann%2Fha-blueprints%2Fmain%2Fblueprints%2Fautomation%2Fnational-siren-test-notification.yaml)

---

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

