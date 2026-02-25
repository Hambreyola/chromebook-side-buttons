# chromebook-side-buttons
Outside of ChromeOS, there is no kernel support/drivers available to get the side volume to work. 
Libinput, xev, and many other tools/scripts fail to recognize them when being pressed, making it impossible to set a keybind to them. 

This project fixes that by talking directly to the chromebook's Embedded Controller (EC) using ectool. 
