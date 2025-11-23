# spotifyd-config

A configuration repository for spotifyd, a lightweight Spotify client daemon. This repo contains a sample and customizable configuration file to enable spotifyd to run with specified user credentials and audio settings.

## Features

- Provides a ready-to-use `spotifyd.conf` configuration file.
- Supports multiple authentication methods including plaintext password, command-based retrieval, and system keyring.
- Configurable audio backend and device settings.
- Supports MPRIS interface for media control integration.

## Tech Stack

- Configuration format: INI-style `.conf` file
- Audio backend: ALSA (Advanced Linux Sound Architecture) by default
- Integration with system services: D-Bus for MPRIS support

## Getting Started

### Prerequisites

- Install `spotifyd` on your system. Refer to [spotifyd GitHub](https://github.com/Spotifyd/spotifyd) for installation instructions.
- Ensure you have ALSA or your preferred audio backend installed and configured.

### Installation

1. Clone this repository:

```bash
git clone https://github.com/justin-napolitano/spotifyd-config.git
cd spotifyd-config
```

2. Edit `spotifyd.conf` to include your Spotify username and password or configure alternative authentication methods.

3. Place the `spotifyd.conf` file in a location where `spotifyd` can access it, typically `~/.config/spotifyd/spotifyd.conf`.

### Running spotifyd

Run spotifyd with the configuration file:

```bash
spotifyd --config-path ~/.config/spotifyd/spotifyd.conf
```

Adjust the path if you place the config file elsewhere.

## Project Structure

- `spotifyd.conf`: Main configuration file for spotifyd. Contains settings for authentication, audio backend, device selection, and D-Bus integration.

## Future Work / Roadmap

- Add support for encrypted password storage or integration with more secure credential managers.
- Expand configuration options to support additional audio backends and platforms.
- Provide example configurations for different operating systems.
- Automate deployment or installation scripts for easier setup.
- Include documentation on troubleshooting common errors related to audio devices or authentication.
