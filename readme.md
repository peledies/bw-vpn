# VPN CLI

## Assumptions

1. `Homebrew` is installed if you are on a Mac
2. You are using `Okta Verify` for MFA with push confrimations turned on
3. You are using `LastPass` as a password manager
4. Your VPN password is stored in LastPass in a record named `bandwidth.com`
5. The `Cisco AnyConnect` client is installed at the following path

```
  /opt/cisco/anyconnect/bin/vpn
```

## Installation

```
curl https://raw.githubusercontent.com/peledies/bw-vpn/main/bw-vpn --output /usr/local/bin/bw-vpn && chmod +x /usr/local/bin/bw-vpn
```

## Configuration

The application will prompt the user for the following variables if they are not set in the environment:

- LASTPASS_EMAIL
- VPN_USERNAME

These variables will be stored in the `~/.bw-vpn/config` file. Once they are set, they can be changed in the file directly or with the bw-vpn tools menu option.
