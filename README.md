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
git clone git@github.com:utzig/lm4tools.git
cd lm4tools
make
cd lm4flash
./lm4flash <binary>
```
