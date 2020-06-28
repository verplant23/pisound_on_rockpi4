# pisound_on_rockpi4
get your incredible pisound from https://blokas.io/ driven by Radxa Rockpi4 rk3399


Thanks to the Armbian Team making build process easy like this, that even me could make things work.
Thanks to pisound team for such a wonderful piece of hardware and making the steps for Tinkerboard.


https://blokas.io/
https://wiki.radxa.com/Rockpi4
https://www.armbian.com/download/


Easy rebuild Kernel/System with these Patches on armbian-buildsystem, or get the debs and install them to your prebuild downloaded from armbian.

Before booting for the first time pisound.dtbo should be moved from / boot / dtb / rockchip / overlay to the previously created / boot / overlay-user folder.
( you can also do it afterwards)
Then add the following entries in the file /boot/armbianEnv.txt
overlays = spi1
user_overlays = pisound

if your rockpi4 has onboard spi... i think this won´t work without changes because cs pin is then  not usable.
with some changes i also got response from nanopim4v2..... but you also have to take care about (re)wiring. to rockpi4 pisound is straight connectable on the header.
