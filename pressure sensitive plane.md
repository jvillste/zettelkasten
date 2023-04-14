The aim is to create a pressure sensitive pane for performing music. An example would be [Soundplane](https://madronalabs.com/soundplane)and [LinnStrument](https://www.rogerlinndesign.com/linnstrument)

Soundpane has a grid of antennas. It sends different frequencies to vertical antennas and reads the signal from horizontal antennas. With furier transform the original signals are separated so that the capacitive coupling of each antenna intersection can be measured.

LinnStrument uses pressure sensitive resistors for pressure sensitivity.

A third approach would be to have the same kind of antenna grid as in Soundplane but we would measure the capacitance of each antenna junction as described in:
[https://embedded-lab.com/blog/making-a-digital-capacitance-meter-using-microcontroller](https://embedded-lab.com/blog/making-a-digital-capacitance-meter-using-microcontroller/) We would need multiplexer banks to raise voltage of each vertical antenna at a time and to measure the capacitance between horizontal and vertical antennas each horizontal antenna at a time. The multiplexer banks could be assembled from surface mounted devices for example from [https://jlcpcb.com/](https://jlcpcb.com/).

To have the same resolution and range as in LinnStrument, we would need at least four junctions in each of the 200 pads. If it's too slow to read each of the 800 junctions one at a time, we could have multiple PIC16F628A microcontrollers (3$/each). Each of them could measure one junction parallelly. The results could be read by forming a parallel bus between the PIC:s and a master micro controller. One PIC would be connected to the master microcontroller at a time again using a multiplexer bank. Also a multiplexer is needed to connect the PIC:s to the vertical antennas.

If we would have 8 PIC:s, 48 horizontal antennas and 16 vertical antennas and we would want to measure every junction 1000 times each second, each measurement and data transfer between the PIC:s and the master microcontroller would need to happen in  `1s/1000/(48*16)*8=10.4us` The capacity measurement is a compromise between used time and resolution. If we want to have 256 levels of resolution and we use 4 MHz clock to measure the time it takes for the current between the antenna pair to raise, we need 256/4000000s = 64us.

FPGA:s could be of use also: [https://tinyfpga.com/](https://tinyfpga.com/)