# Fibocom L8x0 Connect for Windows

![](./screenshot/screen01.png)

## Run

All script **_must_** be run as administrator

- `connect.cmd`: Connect and monitoring
- `connect_with_logs.cmd`: Connect and monitoring. With logging
- `monitor.cmd`: Connection monitoring without connect
- `monitor_with_logs.cmd`: Connection monitoring without connect. With logging

## Setup

#### APN

Edit `scripts/main.ps1` to configure your carrier APN, APN_USER and APN_PASS

#### Preferred bands

Find `AT+XACT=` in `scripts/main.ps1` and edit command to your needs
Example:

- UMTS+LTE all bands, LTE preferred: AT+XACT=4,2,,0
- LTE all bands: AT+XACT=2,,,0
- LTE 3 and 7 bands: AT+XACT=2,,,103,107

### Override DNS

Edit `scripts/main.ps1` to configure your DNS: DNS_OVERRIDE

### Override COM Port

If you don't have ACM2 com ports in your system, you should edit name `$COM_NAME` into `scripts/main.ps1`
