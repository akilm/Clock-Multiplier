# Clock-Multiplier
On-chip Clock multiplier (pll) (Fclkin – 5MHz to 12Mhz, Fclkout – 40MHz to 100MHz at 1.8v@osu180nm)

This project aims at developing an On-chip Clock Multiplier based on Phase-locked loops. Clock Multipliers are used in a variety of VLSI chips to provide high frequency clock signals. Detailed steps to view the schematic and waveforms are mentioned below.


## Tool Used
```LTspice``` is used to simulate the Clock-Multiplier. Ltspice is a spice
simulation software produced by semiconductor manufacturer Analog Devices. This spice tool
is one of the easiest SPICE tool with an user-friendly GUI to display the Schematic of circuits and the waveforms .

## LTspice Installation Guide
LTspice installation steps are described for all kinds of users: Windows, Mac and Linux operating systems.

### Windows and Mac

1. Download the setup file from Analog Devices webpage or click on the download link below for redirecting to the download page. 
   [LTSpice Download for Windows and MAC](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html)
2. Click on ```Download for Windows``` or ```Download for Mac```  according to your requirements to download the setup file.
3. Now follow basic installation steps and install the software.

### LINUX

1. LTspice is not directly supported on LINUX distributions. 
2. LINUX users must install WINE. Wine is a linux software that creates windows environment and allows you to run various windows programs. Download wine from Wine.
3. Download LTspice setup for windows from DOWNLOAD .Click on ```Download for windows``` 
4. Right click on the downloaded setup file and select the option ```Open With > Wine Windows Program Loader```
5. Accept the license and follow basic installation steps.

### LTspice Getting Started

The different features of LTspice are described briefly in [LTspice Getting Started Guide](https://www.analog.com/media/en/simulation-models/spice-models/LTspiceGettingStartedGuide.pdf?modelType=spice-models)
## Simulations
The Steps to run the simulations and view the necessary waveforms are described briefly in this section.
### View Schematic 

The following steps should be followed to view the schematic:

1. Clone the repositary in your desktop or download the zip file and extract all files into
your pc. \n
2. Open ``` LTspice ```and follow the following steps
 ``` File > Open > Select the .asc files ```. 
3. Once you have opened the file. You can see the spice schematic.

###### Phase Frequency Detector

###### Low-Pass Filter and Amplifier 

###### Voltage Controlled Oscillator (Ring Type)


### View Waveforms 

The following steps should be followed to view the waveforms:

1. To view the waveforms just click the Simulate tab on the top and select Run
option which opens a waveform window for you.
2. Go to schematic and click the nodes at which you wish to view the waveforms.
3. To view the various node voltages in different plots simultaneously, just right click on the
waveform window and select Add Plot Pane. This will add an extra pane to view the wave forms.
You can add as many number of panes according to your requirement.
4. If you feel like changing the color of the waveforms or background, ```Tools > Control Panel > Waveforms > Color Scheme.```

###### Reference and Output Clock Frequency Waveforms

### Spice Netlist
You can also view the spice netlist of your schematic. View > Spice Netlist.
A text box that contains the spice netlist opens up.
Follow the following steps to use the spice netlist to view your waveforms:

1. Copy the spice netlist to notepad and save the file with extension as .cir.
2. Open LTspice and drag the .cir file into the LTspice window, which opens the netlist in LTspice.
3. Type the command .print XX below the command .tran . Here XX denotes the label of the quantity used.
4. To view the waveforms just click the Simulate tab on the top and select Run
option which opens a waveform window along with the waveform of the node mentioned in the previous step.

If any wrong label is entered, a dialogue box opens containing the list of all nodes and labels available.
