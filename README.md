# ncas-flux-2-tools

Consisting of scripts for the MOXA data acquisition device, based on that used in the TEAMx deployment in Summer 2025.

## home/bin/checklogger

Tries to check that the logger is running and starts it if not. Assumes `/home/logger.pid` contains the PID of the logger.

## home/bin/checknetwork

If the configured interface (usually `eth1`) comes up before the DNS server has give out IPs, it will need restarting - this script checks and restarts as needed.
