# Setup Steps:
- Flash the latest OS to an sd card, with the [Raspberry Pi Imager](https://www.raspberrypi.com/software/), making sure to enable ssh and change the default credentials
- Follow instructions [here](https://github.com/morrownr/8821cu-20210916) to set up wifi adapter drivers.
- Use [this](https://www.tomshardware.com/how-to/raspberry-pi-access-point) guide to set the pi up as an access point. **MAKE SURE THAT YOU USE `wlan1` FOR THE AP, OTHERWISE YOU WILL BE UNABLE TO CONNECT HEADLESSLY**
- Install [WebSSH](https://github.com/huashengdun/webssh)
- Edit `/etc/rc.local` to incude a line like `sudo /home/thetrail/WebSSH/bin/wssh --address="0.0.0.0" --port="80" &` according to [this](https://www.dexterindustries.com/howto/run-a-program-on-your-raspberry-pi-at-startup/) guide. **DO NOT FORGET THE AMPERSAND AT THE END**
