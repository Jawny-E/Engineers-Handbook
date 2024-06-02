---
banner: "![[resistors.jpg]]"
banner_y: 0.31
---
Are the most basic forms circuits found electrical applications. Resistive circuits behave linearly and consists of basic elements. 
**You should have a grasp on these topics**
- [[#Ohm's Law|Ohm's Law]]
- [[#Kirchoff's Law|Kirchoff's Law]]
- [[#Single Loop Circuits|Single Loop Circuits]]
- [[#Single Node-Pair Circuits|Single Node-Pair Circuits]]
- [[#Series and Parallel Resistors|Series and Parallel Resistors]]
- [[#Wye - Delta Transformation|Wye - Delta Transformation]]
- [[#Dependent Sources in Circuits|Dependent Sources in Circuits]]
- [[#Examples and Problems|Examples and Problems]]

## Ohm's Law
> [!CITE] Ohms's Law
> The voltage across a resistance is directly proportional to the current flowing through it. The resistance, measured in Ohms (Ω), is the constant of proportionality between the voltage and the current. 

Electrical components which are mostly resistive in nature are called [[Resistors|resistors]] and are usually wire-wound or made with metal films.
###### The mathematical relationship of Ohm's Law
$$
\begin{align}
v(t)=R\cdot i(t), where R \geqslant 0
\tag{2.1}
\end{align}
$$

By definition we also have that $1\Omega =1\frac{V}{A}$

It is important to note that we assume the resistors are linear. In real life applications these components will exhibit non-linear  behaviour. 

###### Instantaneous power for resistive circuit
As indicated earlier the rate of energy dissipation in a resistor is the instantaneous power, and therefore we can rewrite the function for power:
![[Basic Concepts#Voltage multiplied with current]]

$$
\begin{align}  \\
p(t)=v(t)\cdot i(t)
\tag{2.2} \\\\
v(t) = R\cdot i(t) \quad\mathrm{and}\quad i(t)=\frac{v(t)}{R}
 \\ \\
p(t)=R\cdot i^2(t)=\frac{v^2(t)}{R}
\tag{2.3}
\end{align}
$$
This equation illustrates that the power is a **non-linear** function of either current or voltage and that it is always a positive quantity (absorbs power).
###### Conductance
The inverse of the resistance is the *conductance* measured in Siemens. Therefore the following expressions apply:
$$
\begin{align} 
G=\frac{1}{R}
\tag{2.4} \\ \\
1S = 1\frac{A}{V} \\ \\
i(t)=G\cdot v(t)  
\tag{2.5} \\\\
p(t)=\frac{i^2(t)}{G}=G\cdot v^2(t)
\tag{2.6}
\end{align}
$$

## Kirchoff's Law

To further study electronic circuits we need to employ some terminlogy: nodes, loops, meshes and branches.
![[node-loop.jpg]]
Given these definitions we can now discuss Kirchoff's circuit laws. Named after German scientist Gustav Robert Kirchoff(1824-1877). 
###### Kirchoff's Current Law (KCL)
> [!CITE] Kirchoffs Current Law(KCL)
> The algebraic sum of the currents entering any node is zero
> $$\sum_{j=1}^{N}i_j(t)=0\tag{2.7}$$
###### Kirchoff's Voltage law (KVL)
> [!CITE] Kirchoffs Voltage Law(KVL)
> The algebraic sum of voltages around any loop is zero. 
> $$\sum_{j=1}^{N}v_j(t)=0\tag{2.8}$$

## Single Loop Circuits
##### Problem Solving Strategy 
1. Define a current *i(t)*. We know using KCL that there is only one current for a single-loop circuit. This current is assumed to be flowing either clockwise or counterclockwise around the loop
2. Using [[Resistive Circuits#Ohm's Law|Ohm's law]], define a voltage across each resistor in terms of the defined current
3. Apply [[Resistive Circuits#Kirchoff's Voltage law (KVL)|KVL]] to the single-loop circuit
4. Solve the single KVL equation for the current *i(t)*. If *i(t)* is positive the current is flowing in the assumed direction
##### The Voltage Divider
![[Pasted image 20240602223012.png]]
To start of with we assume that the current goes in a clockwise direction. We have also assigned a voltage polarity for $v_{R_1}$ and  $v_{R_2}$. Applying [[Resistive Circuits#Kirchoff's Voltage law (KVL)|KVL]] to this circuit gives us the following:
$$
\begin{align}
-v(t)+v_{R_1}+v_{R_2} = 0\\
v_{R_1}+v_{R_2} =v(t) \\
\end{align}
$$
Further from Ohm's law we can find that 
$$
\begin{align}
v_{R_1} = R_1\cdot i(t)\\
v_{R_2} = R_2\cdot i(t) \\
\end{align}
$$
Combining the KVL and Ohms analysis we can find that:
$$
\begin{align}
v_{R_1}+v_{R_2} =v(t) \\ \\
R_1\cdot i(t)+R_2 \cdot i(t) = v(t) \\ \\
i(t)=\frac{v(t)}{R_1+R_2}
\tag{2.9}
\end{align}
$$
If we know the current we can now find the Voltage across each resistor:
$$
\begin{align}
v_{R_1}=R_1\cdot i(t)\\ \\
= R_1\left[ \frac{v(t)}{R_1+R_2} \right]\\ \\
=\frac{R_1}{R_1+R_2}\cdot v(t)\tag{2.10}
\end{align}
$$
For $v_{R_2}$ we complete a similar calculation:
$$
\begin{align}
v_{R_2}=\frac{R_2}{R_1+R_2}\cdot v(t)\tag{2.11}
\end{align}
$$
Having solved all of this the equations we can now see that this fulfils Kirchoffs Voltage Law since we have that
$$
\begin{align}
\frac{R_1}{R_1+R_2}\cdot v(t)+\frac{R_2}{R_1+R_2}\cdot v(t)=v(t)
\end{align}
$$

##### Multiple sources and resistors
Whenever you have a single-loop circuit of passive components your end goal should always be to find the **equivalent circuit**
## Single Node-Pair Circuits
![[Resistive Circuits#Single Loop Circuits#Problem Solving Strategy]]#

## Series and Parallel Resistors

## Wye - Delta Transformation

## Dependent Sources in Circuits

## Examples and Problems



