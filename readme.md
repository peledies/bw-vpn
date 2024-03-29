# VPN CLI

![bw-vpn screenshot](/bw-vpn.png?raw=true "bw-vpn screenshot")

## Assumptions

1. `Homebrew` is installed if you are on a Mac
2. You are using `Okta Verify` for MFA with push confrimations turned on
3. The `Cisco AnyConnect` client is installed at the following path

```
  /opt/cisco/anyconnect/bin/vpn
```

## Installation

```
sudo curl https://raw.githubusercontent.com/peledies/bw-vpn/main/bw-vpn --output /usr/local/bin/bw-vpn && sudo chmod +x /usr/local/bin/bw-vpn
```

## Updating

Its easy! Just select `update` from the main menu. Is going to run the install `curl` again so it will need your `sudo` password.

## Configuration

The application will prompt the user for the following variables if they are not set in the environment:

- LASTPASS_ENABLED=boolean
- VPN_USERNAME=string
- VPN_ENDPOINT=string
- LASTPASS_EMAIL=string
- LASTPASS_KEY_NAME=string

These variables will be stored in the `~/.bw-vpn/config` file. Once they are set, they can be changed in the file directly or with the bw-vpn tools menu option.


## Pre-selections
pre selections for the following VPN prompts can be overridden in the configuration section:

- Okta authentication method
- VPN network