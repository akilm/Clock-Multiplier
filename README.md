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

1. LTspice is not directly supported on LINUX distributions. Wine is a linux software that creates windows environment and allows you to run various windows programs.
2. Click here to install [WINE](https://wiki.winehq.org/Download).
3. Download LTspice setup for windows from [LTSpice Download for Windows](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html).Click on ```Download for windows``` .
4. Right click on the downloaded setup file and select the option ```Open With > Wine Windows Program Loader```
5. Accept the license and follow basic installation steps.

### LTspice Getting Started

The different features of LTspice are described briefly in [LTspice Getting Started Guide](https://www.analog.com/media/en/simulation-models/spice-models/LTspiceGettingStartedGuide.pdf?modelType=spice-models)
## Simulations
The Steps to run the simulations and view the necessary waveforms are described briefly in this section.
[TSMC180nm](https://user.eng.umd.edu/~newcomb/courses/spring2010/303/tsmc180nmcmos.lib) library is used for simulating the circuit. Need to Change the Library to Osu180nm.
### View Schematic 

The following steps should be followed to view the schematic:

1. Clone the repositary in your desktop or download the zip file and extract all files into
your pc. \n
2. Open ``` LTspice ```and follow the following steps
 ``` File > Open > Select the .asc files ```. 
3. Once you have opened the file. You can see the spice schematic.

The schematic is divided into the following components : namely ```Phase Frequency detector```,``` Charge Pump```, ```Low-Pass Filter``` ,```Amplifier ``` and ```Voltage Controlled Oscillator```. Working on the ```Frequency Divider``` Section on the feedback path, it will be updated soon along with the schematic file.

#### Phase Frequency Detector
![alt text](https://github.com/akilm/Clock-Multiplier/blob/master/Schematic%20and%20Waveform%20images/Phase%20Frequency%20Detector.JPG)
<br /> Dual D type phase frequency detector is implemented with both the D inputs connected to Vdd. CLK1 forms the reference frequency and CLK2 is the output frequency. 
#### Charge Pump, Low-Pass Filter and Amplifier 
![alt text](https://github.com/akilm/Clock-Multiplier/blob/master/Schematic%20and%20Waveform%20images/ChargePump%20LpF%20and%20Amplifier.JPG)
<br /> QCLK1(Up) and QCLK1(Down) signals are fed as inputs to the charge pump.The control voltage for the ring oscillator is obtained from the output of the amplifier stage.
#### Voltage Controlled Oscillator (Ring Type)
![alt text](https://github.com/akilm/Clock-Multiplier/blob/master/Schematic%20and%20Waveform%20images/Ring%20Oscillator.JPG)
<br /> A 5-stage Current starved Ring Oscillator is implemented as show in the schematic.Vcont acts as the controlling voltage signal for the output frequency CLK2.
#### View Waveforms 

The following steps should be followed to view the waveforms:

1. To view the waveforms just click the Simulate tab on the top and select Run
option which opens a waveform window for you.
2. Go to schematic and click the nodes at which you wish to view the waveforms.
3. To view the various node voltages in different plots simultaneously, just right click on the
waveform window and select Add Plot Pane. This will add an extra pane to view the wave forms.
You can add as many number of panes according to your requirement.
4. If you feel like changing the color of the waveforms or background, ```Tools > Control Panel > Waveforms > Color Scheme.```

#### Reference and Output Clock Frequency Waveforms
![alt text](https://github.com/akilm/Clock-Multiplier/blob/master/Schematic%20and%20Waveform%20images/Clk%20waveforms.JPG)
<br /> Input (CLK1) and Output (CLK2) Waveforms
![alt text](https://github.com/akilm/Clock-Multiplier/blob/master/Schematic%20and%20Waveform%20images/VCO%20Control%20Voltage.JPG)
<br /> Control Voltage for Ring Oscillator.
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

