# dump1090 for Raspberry pi 3 and Docker

Requirements:

- Raspberry pi with docker daemon
- RLT_SDR USB Device connected to the raspberry pi

## Web interface

```bash
docker run --name dump1090 -d -p 8080:8080 --privileged -v /dev/bus/usb:/dev/bus/usb albertsola/rpi3-dump1090:latest
```

Then visit http://{raspberry_ip}:8080

## Console interactive

```bash
docker run --rm -ti --privileged  -v /dev/bus/usb:/dev/bus/usb albertsola/rpi3-dump1090:latest /usr/local/dump1090/dump1090 --interactive

```