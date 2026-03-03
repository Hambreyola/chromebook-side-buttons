# chromebook-side-buttons
Outside of ChromeOS, there is rarely kernel support/drivers available to get chromebook side volume button functionality. 
Libinput, xev, evtest, and many other programs fail to recognize them, let alone detect when pressed, making it impossible to set a keybind to them. 

This project fixes that by communicating directly with the chromebook's Embedded Controller (EC) using ectool (learn more at https://docs.chrultrabook.com/docs/installing/ectool.html). 

However, communicating with the EC is more of a workaround solution and comes with some downsides. Currently, this project runs a bash script that constantly loops every 0.05s to detect when the EC fires a side button event. This approach is qutie ineffecient, and on lower end devices, uses up ~2% of the CPU for this single task. This is being actively worked on by attempting different approaches to the problem at hand.

## CURRENTLY IN ALPHA DEVELOPMENT.
