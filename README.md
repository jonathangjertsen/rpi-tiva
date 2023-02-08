```sh
sudo nano /etc/udev/rules.d/61.stellpad.rules
```

Write the following:

```
SUBSYSTEM=="usb", ATTRS{idVendor}=="1cbe", ATTRS{idProduct}=="00fd", MODE="0666"
```

Then
```
sudo udevadm trigger
sudo apt-get install libusb-1.0.0-dev make pkg-config build-essential
git clone https://github.com/utzig/lm4tools.git
cd lm4tools
make
cd lm4flash
./lm4flash <binary>
```
