# HostsLion

A `hosts` file used to block out ads, trackers and malware specific to Czech websites.

## What is a `hosts` file?

A `hosts` file is a plain-text file used by operating systems to map hostnames to IP addresses. By mapping hostnames serving unwanted content to a non-existent domain, we can prevent any outgoing connections to this domain.

## How to use a `hosts` file?

Using a `hosts` file in your system can be easy. There are several ways how to do it so pick the one that works best for you.

### Using a manager

An easy way to add this `hosts` file to your computer is to use a manager app, such as [SwitchHosts!](https://oldj.github.io/SwitchHosts/) (available for Mac, Windows and Linux).

You can copy and paste the contents of _HostsLion_ to your manager but you would miss on any potential future updates. A better way is to add our `hosts` file's URL so that your computer always stays up to date.

### Manually editing your `hosts`

If for some reason you don't wish to use manager app, you can also add the records from _HostsLion_ to your local `hosts` file manually.

- Mac, Linux and other Unix-based systems: `/etc/hosts`
- Windows: `%SystemRoot%\system32\drivers\etc\hosts`

You might need administrator privileges to save any changes to your `hosts` file.

Also, don't forget to restart your DNS service:

- Mac, Linux and other Unix-based systems: `sudo killall -HUP mDNSResponder`
- Windows: `ipconfig /flushdns`

### Pi Hole

Perhaps the most convenient way to use _HostsLion_ is through the network-wide protection of [Pi-hole](https://pi-hole.net/).

You can set up a cheap Raspberry Pi such as the Zero (and an optional Ethernet module such as the ENC28J60) to act as a DNS server for all your devices. This will protect all your computers, mobile phones, tablets and other devices where software protection might be limited and manual editing of the `hosts` file outright impossible.

See the [Pi-hole documentation](https://docs.pi-hole.net/) for more information.
