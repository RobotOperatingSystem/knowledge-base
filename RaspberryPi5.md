# Tweaking Raspberry Pi 5

## Preparing Pi OS

Install official Raspberry Pi imager:

```shell
$ sudo dnf install rpi-imager 
```

Insert SD card. Make sure the read-only switch on the card extender is in position `write`.

Run the imager:

```shell
$ rpi-imager
```

Select the Raspberry Pi model: `RASPBERRY PI 5`

Select the operating system: `RASPBERRY PI OS (64-BIT)`

Select the mounted SD card.

Write the image.
