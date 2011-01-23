*** MindSetBTViewer Install Instructions ***

Written by Dr. Sean M. Montgomery - http://produceconsumerobot.com/
with super awesome MindSet library written by Rob King (http://addi.tv) in collaboration with the Mobile Lab at Ontario College of Art and Design (http://mobilelab.ca/).
Please let me know if you have any problems.

Below are the instructions to use the MindSetBTViewer processing script to read, plot, and log data from the NeuroSky MindSet directly over your computer's bluetooth connection.


Materials:
1	NeuroSky MindSet
1	Computer


Required Software (see below for download instructions):
Processing
MindSet Library
Arduinoscope library
ControlP5 library
MindSetBTViewer


Instructions:

Follow the instructions that came with your MindSet to connect the MindSet to the Bluetooth port on your computer. Briefly, after installing the software on the CD, plug in the accompanying Bluetooth module, turn on the MindSet and put the headset into discovery mode by holding the play button until the red and blue lights on the MindSet flash. Open the Bluetooth settings on your computer and add a new Bluetooth device in custom mode. Choose the MindSet and add a connection to the serial port. Note the specific serial port that your MindSet is connected to (e.g. COM41) -- you will need it later. Finally, connect to the MindSet using the passkey 0000. You can test whether your MindSet is working properly with NeuroSky’s Brainwave Visualizer.

Download and extract Processing software
http://processing.org/download/
getting started - http://processing.org/learning/gettingstarted/

Download MindSet library
http://addi.tv/mindset/

Download Arduinoscope library
http://arduinoscope.googlecode.com/files/processing-arduinoscope.zip
getting started -  http://code.google.com/p/arduinoscope/wiki/Usage
optional downloads - http://code.google.com/p/arduinoscope/downloads/list

Download ControlP5 library
http://www.sojamo.de/libraries/controlP5/

In the processing\libraries\ directory
unzip contents of MindSet
unzip contents of processing-arduinoscope.zip
unzip contents of controlp5.zip
Directory structure should be:
processing\libraries\MindSet\library\
processing\libraries\arduinoscope\examples\
processing\libraries\arduinoscope\library\
processing\libraries\arduinoscope\reference\
processing\libraries\arduinoscope\src\
processing\libraries\controlP5\examples\
processing\libraries\controlP5\library\
processing\libraries\controlP5\reference\
processing\libraries\controlP5\src\

Download and extract MindSetBTViewer from 
https://github.com/produceconsumerobot/MindSetBTViewer

Open MindSetBTViewer.pde with processing.

Change String serialPort = "COM1"; to whatever bluetooth serial port your MindSet is connected to (e.g. COM41).

Hit Run. If you want to record data, press the green record button. You must have write privileges in your processing directory or change the directory specified in MindSetBTViewer.pde. You may change the y-scale of the individual plots using the "*2" and "/2" buttons or in the user-variable section of the code.

If you haven’t already, put the MindSet on your head and try to get a good EEG signal. Look for low background noise in the Raw EEG and low ErrorRates as seen in the top panel of "signal_quality.jpg". Note how you can clearly see eyeblinks on a low noise background indicating a a high quality signal in the top panel, while in the lower two panels it is not possible to distinguish eyeblinks from background noise. Many times you will get a good signal very quickly, but depending on several factors it can take as much as 30 seconds or more for the MindSet to settle into a good signal. To speed up that process it can be quite helpful to dab your forehead and ear with some salt water (1/4 teaspoon of salt in a cup of water works).



