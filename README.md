# ukw_bandstop
## Bandstop filter on a small PCB to eliminate strong UKW (87.5 - 108 MHz) broadcast signals.

FM radio broadcast signals are usually really strong compared to e.g. ham radio short wave signals. The FM signals can cause massive intermodulation in SDRs, LimeSDR in my case. So I designed a small prototype of a filter for these frequencies.

### Calculation
I used the free version of Ansoft Designer for the calculation of the filter. Parameters were:
* Legendre approximation
* Stop band from 80 to 120 MHz
* Order 5

After calculation I had to tune/round the values of Cs and Ls to existing components.

### PCB design
The input and output are SMA connectors. All other components are 0603 SMD.

### First prototype
The first prototype was ordered at dirtypcbs. 

### Results
I soldered one board and measured with my Siglent SSA 3021X spectrum analyzer, see screenshot. 
You can see the corner frequencies at 73 and 140 MHz.