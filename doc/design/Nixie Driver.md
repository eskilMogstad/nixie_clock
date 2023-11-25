
# Old school drivers
## 74141

![[figures/74141_1.gif]]
![[figures/74141_2.gif]]

## K155ID1
# Newer drivers

## HV5530

300 V inputs
32 channels
10.8-13.2 V logic supply, 12V nominal

![[figures/Pasted image 20231119121128.png]]

32 channels per times 2 chips gives 64 inputs

6 digits (10 states) + 2\*2 semicolons also yields 64 inputs, so two of these is perfect for the application

Just have to levelshift the microcontroller output signals to 12V logic


# Current limiting

The current flowing through the nixie tube has to be limited, which can be done using a resistor

A schematic of the drive circuit is shown below.
Assuming the voltage drop across the MOSFET is negligible, the current follows the following equation

$$
I = \frac{V-V_N}{R}
$$
![[figures/Nixie driving diagram.svg|200]]
For the IN-12, the sustain voltage is around 145V
$$R = 15 k\Omega$$

For the INS-1, the sustain voltage is 55 V, recommended current 0.5 mA

$$R = 60 k\Omega$$



