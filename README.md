# hostosx
## TL;DR
Use the native MacOS X/macOS mechanisms to perform forward and reverse DNS lookups on the command-line.

A tiny command‑line utility for macOS that performs forward and reverse DNS lookups using the system’s native resolver. `hostosx` aims to behave like the classic `host`/`dig` workflows while relying on macOS APIs and configuration.

## Why hostosx?
Tools like the Internet [Software|Systems] Consortium's `host`, `nslookup`, `dig`, as Apple declares in those commands' man pages, don't, "use the host name and address resolution or the DNS query routing mechanisms used by other processes running on macOS. The results of name or address queries printed by host may differ from those found by other processes that use the macOS native name and address resolution mechanisms. The results of DNS queries may also differ from queries that use the macOS DNS routing library."
This `hostosx` script aims to provide similar command line use as the traditional ISC tools but resolve lookups in the same way the GUI apps do. 
 
- Uses macOS’s native DNS resolution stack for results that match what the system and apps see.
- Simple, single‑purpose interface for forward (A/AAAA) and reverse (PTR) lookups.
- Helpful, human‑readable output with clear exit codes suitable for scripts.

## Features
- Forward lookups from hostname to IP addresses (IPv4 and IPv6)
- Reverse lookups from IP address to hostname (PTR)
- Respects system resolver configuration and search domains
- Minimal dependencies; runs on stock macOS
