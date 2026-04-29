# balena-homeassistant

[Home Assistant](https://www.home-assistant.io/) - Open source home automation that puts local control and privacy first.

## Getting Started

You can one-click-deploy this project to balena using the button below:

[![deploy with balena](https://balena.io/deploy.svg)](https://dashboard.balena-cloud.com/deploy?repoUrl=https://github.com/PierrickGT/balena-homeassistant.git)

## Manual Deployment

Alternatively, deployment can be carried out by manually creating a [balenaCloud account](https://dashboard.balena-cloud.com) and application, flashing a device, downloading the project and pushing it via the [balena CLI](https://github.com/balena-io/balena-cli).

### Application Environment Variables

Application envionment variables apply to all services within the application, and can be applied fleet-wide to apply to multiple devices.

| Name           | Description                                                                                                       |
| -------------- | ----------------------------------------------------------------------------------------------------------------- |
| `TZ`           | Inform services of the [timezone](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) in your location. |
| `SET_HOSTNAME` | Set a custom hostname on application start. Default is `homeassistant`.                                           |

## Usage

Once your device joins the fleet you'll need to allow some time for it to download the various services.

### Services

#### adguard

[AdGuard Home](https://adguard.com/adguard-home/overview.html) is a network-wide ad blocking and privacy protection DNS server.

The web interface is running on port 80.

#### netdata

[Netdata](https://www.netdata.cloud/) is a real-time system monitoring and troubleshooting tool.

The dashboard is running on port 19999.

#### hostname

An utility block to set the hostname of devices running balenaOS.

This service is expected to remain in the `stopped` state after applying changes.

<https://github.com/balenablocks/hostname>

#### tailscale

Add your device to your [Tailscale](https://tailscale.com/) network with this block!

<https://github.com/klutchell/balena-tailscale>

## Contributing

Please open an issue or submit a pull request with any features, fixes, or changes.
