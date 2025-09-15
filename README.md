# pfSense Speedtest.net 2 Dashboard Widget

A pfSense dashboard widget that runs a Speedtest.net test using the official Ookla CLI and displays results directly in the pfSense dashboard. Forked from https://github.com/LeonStraathof/pfsense-speedtest-widget

✅ **Tested on:**  
pfSense **2.8.0-RELEASE (amd64)**  
Built on Thu May 22 07:12:00 PST 2025  
FreeBSD **15.0-CURRENT**

---

## Screenshot

![Screenshot](https://github.com/woots29/pfsense-speedtest-widget/blob/main/speedtest2_screenshot.JPG?raw=true)

---

## Features

- Selects **real interface** (e.g. `pppoe0`, `ix1.100`) instead of logical interface names
- Uses official [Ookla Speedtest CLI](https://www.speedtest.net/apps/cli)
- Displays **Download, Upload, Ping, Server, ISP**
- Compatible with pfSense 2.8.0 / FreeBSD 15.0-CURRENT  

---

## Installation

> ⚠ **Disclaimer:**  
> This forces installation of the `speedtest` port on FreeBSD 15.0-CURRENT, which is not officially supported. (The latest supported OS for Speedtest is FreeBSD 13 at the time of writing.)
> You are responsible for any risk of breakage.
```	
git clone --depth 1 https://git.FreeBSD.org/ports.git /root/ports
```
```
cd /root/ports/net/speedtest
```
```
env UNAME_r=14.0 ALLOW_UNSUPPORTED_SYSTEM=yes make install clean
```
Then follow the installation procedure by https://github.com/LeonStraathof/pfsense-speedtest-widget

