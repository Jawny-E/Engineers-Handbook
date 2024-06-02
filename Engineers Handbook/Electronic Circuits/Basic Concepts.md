---
banner: "![[pcb.jpg]]"
banner_y: 0.888
---
**Table of Contents**

- [[#System of Units|System of Units]]
- [[#Basic Quantities|Basic Quantities]]
	- [[#Basic Quantities#Charge|Charge]]
	- [[#Basic Quantities#Current|Current]]
	- [[#Basic Quantities#Voltage|Voltage]]
	- [[#Basic Quantities#Energy|Energy]]
	- [[#Basic Quantities#Maths|Maths]]
- [[#Circuit Elements|Circuit Elements]]
	- [[#Circuit Elements#Independent Sources|Independent Sources]]
	- [[#Circuit Elements#Dependent Sources|Dependent Sources]]
- [[#Examples and Problems|Examples and Problems]]

## System of Units
<u>Standard SI prefixes:</u>

| Prefix  | Symbol   | Number                     | Scientific Notation     |
| ------- | -------- | -------------------------- | ----------------------- |
| Exa     | E        | 1'000'000'000'000'000'000  | $10^{18}$               |
| Peta    | P        | 1'000'000'000'000'000      | $10^{15}$               |
| Tera    | T        | 1'000'000'000'000          | $10^{12}$               |
| Giga    | G        | 1'000'000'000              | $10^{9}$                |
| Mega    | M        | 1'000'000                  | $10^{6}$                |
| Kilo    | k        | 1'000                      | $10^{3}$                |
| Hecto   | h        | 100                        | $10^{2}$                |
| Deka    | da       | 10                         | $10^{1}$                |
| ------- | -------- | 1                          | ----------------------- |
| Deci    | d        | 0.1                        | $10^{-1}$               |
| Centi   | c        | 0.01                       | $10^{-2}$               |
| Milli   | m        | 0.00'1                     | $10^{-3}$               |
| Micro   | μ        | 0.00'000'1                 | $10^{-6}$               |
| Nano    | n        | 0.00'000'000'1             | $10^{-9}$               |
| Pico    | p        | 0.00'000'000'000'1         | $10^{-12}$              |
| Femto   | f        | 0.00'000'000'000'000'1     | $10^{-15}$              |
| Atto    | a        | 0.00'000'000'000'000'000'1 | $10^{-18}$              |

## Basic Quantities

### Charge
The most elementary quantity in an analysis of electrical circuits is the *electric charge*. One can define a circuit as a pipeline that facilitates the transfer of charge between points. The rate of change constitutes the *electric current*. And we can mathematically describe this relationship as shown in equation:

$$
\begin{align}
i(t) = \frac{dq(t)}{dt} 
\quad\mathrm{or}\quad   q(t) = \int_{-\infty}^{t}i(x)dx
\tag{1.1}
\end{align}
$$
### Current
The basic units for current and charge are *i* and *q* respectively. The basic unit for current is Ampere(A) and is defined as 1 Coulomb per second. It is important to be definite when defining the direction of the current flow and always stock to that definition. 
In our daily lives we encounter two types of current: *Alternating* or *Direct* current. Noted as AC or DC. 

### Voltage
The electronic *voltage* is defined as the difference in energy level of a unit of charge located at each of the two points. It is noted as v(t) or simply V. As a thought experiment you can imagine that the Voltage pushes the charge through the inductor. 

### Energy
Energy or work w(t) or W, is measured in Joules: 1 Joule is 1 Newton metre (N$\cdot$m). Hence, voltage is measured in Volts which is equivalent to  1 Joule per Coulomb = 1 Newton metre per Coulomb.  Furthermore we define the change in Energy over time as *Power*. Power is defined in such a way that a positive number denotes an element absorbing power, and a negative number denotes supplying power

### Maths
We have now defined Voltage in Joules per Coulomb as the energy required to move a positive charge of 1C through an element. If we assume we are dealing with a differential amount of charge and energy then we have:
###### Voltage, energy, charge relationship
$$
\begin{align}
v = \frac{dw}{dq}\tag{1.2}
\end{align}
$$
Further we can multiply this with the current to get the energy which is measured in Joules per Second, or Watts
###### Voltage multiplied with current
$$
\begin{align}
v\cdot i =(\frac{dw}{dq})(\frac{dq}{dt}) = \frac{dw}{dt} = p \tag{1.3}
\end{align}
$$
Since *i* and *v* both are functions of time, *p* will also be a time varying quantity. Therefore, we can find the change in energy from time *t<sub>1</sub>*  to time *t<sub>2</sub>* with the following equation:
###### Change in energy over time
$$
\begin{align} 
\Delta w = \int_{t_1}^{t_2}p\space dt = \int_{t_1}^{t_2}vi\space dt \tag{1.4}
\end{align}
$$
<u>Typical Current Magnitudes:</u>

| $10^{6}$   | Lightning Bolt                            |
| ---------- | ----------------------------------------- |
| $10^{4}$   | Large industrial motor                    |
| $10^{2}$   | Typical household appliance               |
| $10^{0}$   | Causes ventricular fibrillation in humans |
| $10^{-2}$  | Human threshold for sensation             |
| $10^{-4}$  |                                           |
| $10^{-6}$  | Integrated Circuit memory cell current    |
| $10^{-8}$  |                                           |
| $10^{-10}$ |                                           |
| $10^{-12}$ | Synaptic current (brain cell)             |
| $10^{-14}$ |                                           |

## Circuit Elements

> [!CITE] Tellegrens Theorem
> The sum of powers absorbed in a network is exactly equal to zero

### The passive sign convention
The passive sign convention states that voltage and current associated with an element are the product of *v* and *i*, with their attendant signs, determines the magnitude and the sign of the power. If the sign is positive, power is being absorbed by the element, and if the sign is negative, the element is supplying power

### Independent Sources
A two-terminal element that maintains a specified voltage or current across its terminals. In their normal mode of operation, these sources supply power to the rest of the circuit. However, depending on connection one can for example use a battery as a independent supply or as a chargeable element. 

### Dependent Sources
In contrast to independent sources, the dependent sources produce a given voltage or current dependent on other factors in the network. MOSFETS and other transistors are examples of elements that are modelled as dependent sources. 

## Examples and Problems
