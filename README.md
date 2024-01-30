# InternetSpeedCalculator-with-GUI
Importing Modules:

import tkinter as tk: Imports the Tkinter module and aliases it as tk for easier reference.
from tkinter import *: Imports all classes and functions from the Tkinter module. This isn't the best practice since it pollutes the global namespace, but it's commonly used in Tkinter code for brevity.
import speedtest: Imports the speedtest module, which is used to perform internet speed tests.
Function speedcheck():

This function is triggered when the "Check Speed" button is clicked.
It creates an instance of Speedtest from the speedtest module.
It fetches the available servers for testing using sp.get_servers().
It calculates the download and upload speeds in Mbps using sp.download() and sp.upload() methods respectively.
It updates the text of lab_down and lab_up labels with the calculated download and upload speeds.
Creating the Tkinter Window (sp):

sp = Tk(): Creates the main application window.
sp.title(" Internet Speed Test"): Sets the title of the window.
sp.geometry("500x650"): Sets the initial size of the window.
sp.config(bg="Blue"): Sets the background color of the window to blue.
Creating Labels and Button:

Labels are used to display text on the window.
lab labels are created for "Internet Speed Test", "Download Speed", and "Upload Speed".
lab_down and lab_up labels are initially set to "00" to display the download and upload speeds.
A button labeled "Check Speed" is created. Its command is set to the speedcheck() function.
Running the Tkinter Application:

sp.mainloop(): Starts the Tkinter event loop, which listens for events (like button clicks) and updates the GUI accordingly.
