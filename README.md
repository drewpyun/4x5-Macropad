# 4x5-Macropad
4x5 Macropad flashing guide 

First download:
QMK Toolkit: https://github.com/qmk/qmk_toolbox

QMK Toolkit will flash a .hex file to the PCB. 

# To get a hex file

We will use this website: https://kbfirmware.com/
Paste the following code into the text box and click "Import"
```
["Num Lock","/","*","-"],
["7\nHome","8\n↑","9\nPgUp","+"],
["4\n←","5","6\n→",{a:7},""],
[{a:4},"1\nEnd","2\n↓","3\nPgDn","Enter"],
["0\nIns",{a:7},"",{a:4},".\nDel",{a:7},""]
```
You should be greeted with something like this--
![Imgur](https://i.imgur.com/l4OTK9O.png)

Click on the "Pins" Tab and change the controller to ATMEGA32**U2** and the Column 3 to **C7** like so.
![Imgur](https://i.imgur.com/SoEI068.png)

Next, configure your keymaps on the keymap and macro tabs.
After you are finished, click on the compile tab, and save the file. 
![Imgur](https://i.imgur.com/r93zhah.png)

Now open up QMK Toolbox and plug in your PCB. 
Change MCU to **atmega32u2**, and open the hex file under local file.

*If the pcb does not register on your computer you may need to hold down the reset switch located on the pcb.*

It should look something like this
![Imgur](https://i.imgur.com/27WxSBN.png)

Click flash.
Your PCB should disconnect and reconnect.
![Imgur](https://i.imgur.com/j3yEomZ.png)

Test your pcb and everything should work!
Contact me at DrewGuy#0718 if you have problems.
