# Flashing or Upgrading your ASP100

---

- [Windows](#windows)
- [Linux](#linux) 

<a name="windows"></a>
## [Windows](#windows)

Two Options for Windows

### Option 1: use command line

### Steps

1. Using command line `dfu-util` is similar to above for Linux / Mac.
2. Highly recommend updating `dfu-util` to the newest version.
3. Download and extract the firmware package from Github [ASPD100 Releases](https://github.com/makanddream/automatic-solder-paste-dispenser/releases).
4. Enter DFU mode: press and hold (-) button at the back of the iron (do not release).
5. Connect USB to PC, and USB-C to the back of Pinecil, keep holding (-) button down.
6. Screen will stay **black/off** to indicate the Pinecil is in DFU mode. This is normal.
7. After the USB cable is connected at both ends, wait ~10 seconds more, then release the (-) button.
8. Open PowerShell or Command window.
9. Change to the directory of the unzipped firmware files
10. Using `dfu-util,`  flash the firmware using a command like this:
```php
dfu-util -D ASPD100_EN.dfu;
```

### Option 2: use the STM32CubeProgrammer gui

### Steps

1. If you are uncomfortable with the command line, then this chip vendor supplied gui tool/drivers is an option.
2. Download and extract the firmware package from Github [ASPD100 Releases](https://github.com/makanddream/automatic-solder-paste-dispenser/releases).
3. Download and install the [STM32CubeProgrammer](https://www.st.com/en/development-tools/stm32cubeprog.html).
4. Enter DFU mode: press and hold (-) button at the back of Pinecil (do not release).
5. Connect Pinecil to a PC via USB cable (do not release the (-) yet).
6. Screen will stay **black/off** to indicate the Pinecil is in DFU mode. This is normal.
7. You may hear a beep from Windows as it connects to Pinecil in DFU mode.
8. If you see windows notification that it `does not recognize Usb device`, then you didn't connect, repeat step 3-8.
9.  Open the GD32 DFU Tool (ignore prompts to update tool).
10. At the top of the DFU tool, you should see `GD DFU DEVICE 1` appear if you successfully connected Pinecil.
11. If DFU Device box at top is blank, then Pinecil is not connected in DFU mode, repeat steps 3-11.
12. If it has been more than 10 seconds since you connected the USB cable, Release the (-) button. (don't use Upload from Device section)
13. Select `Download to device` > Open > Browse to folder dyou unziped in step 2.  
14. Select the `hex` file for language. English is  Pinecil_EN.hex , tick `Verify after download`.
15. Click `OK` at bottom. After a few minutes you will see 0-100%,  Download successfully!  Click `Leave DFU` at the top. 
16. Disconnect pinecil cable from PC, plug it into a power supply.
17. Do not need to press any buttons, a new screen should appear.
18. To confirm upgrade, hold the minus (-) button down for a few seconds, it then shows new firmware version v2.xx.x....date

---

<a name="linux"></a>
## [Linux](#linux)

Todo !!!