# Pawsync Home Assistant Integration

This custom integration allows you to connect your Pawsync pet feeder devices to Home Assistant. You can monitor device status, view sensor data, and trigger feeding actions directly from your smart home dashboard.

## Features

- **Sensor Entities:** Exposes device properties (e.g., food level) as Home Assistant sensors.
- **Feed Service:** Trigger manual feeding via Home Assistant services.

## Installation

1. Copy the `pawsync` directory into your Home Assistant `custom_components` folder.
2. Restart Home Assistant.

### HACS

If you are using HACs just add the repo as a custom repository of type `Integration`.

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
