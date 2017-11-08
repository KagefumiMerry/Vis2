# Vis2 - OCR(), ImageIdentify()
##### Automation using Computer Vision. 

### Quick Start
1. [Download Vis2.](https://github.com/iseahound/Vis2/archive/master.zip) Extract. 
2. Create a new AHK script in the same folder as Vis2.ahk, 
copying the code below. 

    #include Vis2.ahk
    MsgBox % OCR("https://i.stack.imgur.com/sFPWe.png")
    
3. Press ```Enter``` to exit. Visit the image link to confirm the OCR is working correctly. 

## Documentation
### OCR()
How to use OCR() - add the following line to your code.

    #^c:: OCR()

The above line will bring up a user interface that allows selection of text on-screen. 
To input a set of known coordinates, try inputting an array of 4 values, [x, y, w, h]

    text := OCR([0, 0, 430, 150])

This will search the screen from point (0, 0) extending in a rectangle of width 430 pixels and height 150 px. 

Note that the following snippet will also return text

    if ((text := OCR()) = "Vis2")
        MsgBox You have successfully used OCR!
    else
        MsgBox You have found [ %text% ] `, try finding 'Vis2' instead. 

Be sure to visit https://autohotkey.com/boards/viewtopic.php?f=6&t=36047 for help and support. 
