# Hotspot Creator & Monitor

Standalone split of the original app in `microsoftcopilotcodeusedonpi`. Original code and app name kept, with only local-path/update wiring and approved credential removal/prompt changes. The source repository is untouched.

## What it does and needs

Upstream Wi-Fi connection plus wlan1 hotspot and device monitor. Requires two compatible Wi-Fi interfaces, nmcli, arp, avahi-resolve-address and iptables. May disconnect existing networking; block actions require root.

## Run

Use the Pi App Store to install and launch. Installation only checks Bash syntax; it does not run administrative actions or install prerequisites. Read the script before selecting Run.

From an extracted checkout:

```sh
bash app-store.sh install
bash app-store.sh run
```

## Safety and limits

This is the original prototype, not a rewritten or hardware-validated release. Some inherited operations may fail or interrupt the system. Prompts do not guarantee safe recovery. Network passwords are requested locally where needed; no OS password is embedded. Use normal sudo authentication. Don't enter credentials on an untrusted/shared terminal.

Do not run unattended on an important Pi. Keep backups. Only administer systems/networks you own or have permission to use.

Linux checks: Bash syntax and packaging tests pass. Raspberry Pi hardware and non-Linux systems are untested. No privileged action was run during validation.

## Tests

```sh
python3 test_packaging.py
```

Version 1.0.0 is the standalone packaging version, not a claim that inherited features changed.
