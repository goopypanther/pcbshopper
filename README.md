PCBShopper.com Quote Generator
==============================

This [Eagle](https://cadsoft.io/) ULP script is designed to simplify generating quotes on the [PCBShopper.com](http://pcbshopper.com) website, which aggregates quoting services from ~30 PCB fabs around the world.

Parameters such as board size, layer usage, trace width and hole diameter are automatically pulled from your board design and numerous other options are available through dropdown lists. When you're ready, the link at the bottom of the dialog will direct you to PCBShopper.com where the relevant information will already be inserted into the proper fields. You can make any final changes you'd like before hitting Get Prices.

![Screenshot](https://raw.githubusercontent.com/JeremyRuhland/pcbshopper/master/pcbshopper.jpg)

Adding a shortcut button to the eagle layout editor toolbar
-----------------------------------------------------------

1. Copy pcb-shopper.png to the "bin" folder under the EAGLE installation directory.
On a MAC it is:

         /Applications/EAGLE-9.0.0/bin

2. Copy PCBShopper.ulp to the "ulp" folder under the EAGLE installation directory.
On a MAC it is:

        /Applications/EAGLE-9.0.0/ulp

3. 
Open "eagle.scr" file from the "scr" folder
On a MAC it is:

        /Applications/EAGLE-9.0.0/scr

Add the following line within the "MENU" section of "BRD:":

     '[bin/pcb-shopper.png] PCB Shopper : Run PCBShopper.ulp;'\

So it reads something like this:


    BRD:    
        MENU 
             '[bin/designlink.png] Search and order : Run designlink-order.ulp -general;'\
             '[bin/pcb-service.png] PCB Service : Run pcb-service.ulp;'\
             '[bin/snapeda.png] SnapEDA : Run snapeda.ulp;'\
             '[bin/samacsys.png] SamacSys : Run samacsys.ulp;'\
             '[bin/idf-3d.png] Export to IDF 3D format: Run eagleidfexporter.ulp;'\
             '[bin/pcb-shopper.png] PCB Shopper : Run PCBShopper.ulp;'\
        
                ;


---

Disclaimer: I am not officially associated with PCBShopper.com in any way. This script was made possible by collaboration with Bob Alexander, owner of PCBShopper. This script comes with no warranty, you are responsible for checking the accuracy of the quotes generated with your respective fab.

Read a review at the [HACKADAY](http://hackaday.com/2016/09/11/this-eagle-script-gets-quotes-for-your-boards) website
