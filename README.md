HAK5 Rubber Ducky Scripts

__ducky-osx-reverse-shell.txt__ - OSX / MacOS Reverse Shell

setup
```
replace 192.168.1.11 and 8080 with the ip/port of your netcat server (attacking host). 
i like to use my phone to catch the reverse shell - https://termux.com/
run this on your attacking host: nc -l -p 8080
plug the ducky into your target, then take a look at your netcat session.  you have a shell!
```

usb setup
```
you'll need to update the firmware to ducky2.1 (for VIDPID spoofing)
https://github.com/hak5darren/USB-Rubber-Ducky/blob/master/Firmware/Images/duck_v2.1.hex
sudo dfu-programmer at32uc3b1256 erase; sudo dfu-programmer at32uc3b1256 flash --suppress-bootloader-mem duck_v2.1.hex; sudo dfu-programmer at32uc3b1256 reset
```

subvert apple's Keyboard Setup Assistant; create a vidpid.bin to spoof an Apple Keyboard 
```
https://github.com/midnitesnake/USB-Rubber-Ducky/wiki/Keyboard_VID_PID_List
https://github.com/hak5darren/USB-Rubber-Ducky/tree/master/Firmware/Utils/VID_PID_SWAPPER_1.1
```


```
                  .
                .'|     .8
               .  |    .8:
              .   |   .8;:        .8
             .    |  .8;;:    |  .8;
            .     n .8;;;:    | .8;;;
           .      M.8;;;;;:   |,8;;;;;
          .    .,"n8;;;;;;:   |8;;;;;;
         .   .',  n;;;;;;;:   M;;;;;;;;
        .  ,' ,   n;;;;;;;;:  n;;;;;;;;;
       . ,'  ,    N;;;;;;;;:  n;;;;;;;;;
      . '   ,     N;;;;;;;;;: N;;;;;;;;;;
     .,'   .      N;;;;;;;;;: N;;;;;;;;;;
    ..    ,       N6666666666 N6666666666
    I    ,        M           M
   ---nnnnn_______M___________M______mmnnn
         "-.                          /
  __________"-_______________________/_________
  ```
