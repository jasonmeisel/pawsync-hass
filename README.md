# Pawsync Home Assistant Integration

This custom integration allows you to connect your Pawsync pet feeder devices to Home Assistant. You can monitor device status, view sensor data, and trigger feeding actions directly from your smart home dashboard.

[![HACS Custom](https://img.shields.io/badge/HACS-Custom-41BDF5.svg)](https://github.com/hacs/integration)
[![HACS Action](https://github.com/jasonmeisel/pawsync-hass/actions/workflows/validate.yaml/badge.svg)](https://github.com/jasonmeisel/pawsync-hass/actions/workflows/validate.yaml)
[![GitHub release](https://img.shields.io/github/v/release/jasonmeisel/pawsync-hass)](https://github.com/jasonmeisel/pawsync-hass/releases)
[![License](https://img.shields.io/github/license/jasonmeisel/pawsync-hass)](LICENSE)

> This integration is not affiliated with or endorsed by Pawsync.

## Features

- **Sensor Entities:** Exposes device properties (e.g., food level) as Home Assistant sensors.
- **Feed Service:** Trigger manual feeding via Home Assistant services.

## Installation

### HACS

1. Select the button below to add this repository to HACS:

[![Open your Home Assistant instance and open a repository inside the Home Assistant Community Store.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=jasonmeisel&repository=pawsync-hass&category=integration)

2. Select **Add**, then **Download** the integration.
3. Restart Home Assistant.
4. Select the button below to configure Pawsync:

[![Open your Home Assistant instance and start setting up a new integration.](https://my.home-assistant.io/badges/config_flow_start.svg)](https://my.home-assistant.io/redirect/config_flow_start/?domain=pawsync)

### Manual installation

1. Copy this repository's contents into `custom_components/pawsync`.
2. Restart Home Assistant.
3. Go to **Settings > Devices & Services > Add Integration** and search for **Pawsync**.

## Configuration

### UI Setup

1. Go to **Settings > Devices & Services**.
2. Click **Add Integration** and search for "Pawsync".
3. Enter your Pawsync account credentials.

### YAML Setup (optional)

Add to your `configuration.yaml`:

```yaml
pawsync:
  username: your_email@example.com
  password: your_password
```

## Services

### Feed

Trigger a manual feeding for a device:

```yaml
service: pawsync.feed
data:
  entity_id: sensor.pawsync_device_id
```

## License

MIT

## Disclaimer

This integration is not affiliated with or endorsed by Pawsync.
