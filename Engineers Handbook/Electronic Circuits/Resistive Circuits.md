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
Whenever you have a single-loop circuit of passive components your end goal should always be to find the **equivalent circuit**. In this simple chapter this means condensing the sources and resistors to as few components as possible applying [[Resistive Circuits#Kirchoff's Current Law (KCL)|KCL]] and [[Resistive Circuits#Kirchoff's Voltage law (KVL)|KVL]].
It is here noted that the *equivalent resistance of N resistors in series is simply the sum of all individual resistances*
## Single Node-Pair Circuits
##### Problem Solving Strategy 
1. Define a voltage *v(t)* between the two nodes of the circuit. [[#Kirchoff's Voltage law (KVL)|KVL]] tells us that there is only one voltage for a single node-pair-circuit.  A polarity is assigned to the voltage such that one of the nodes is assumed to be at a higher potential than the other node, which we will call the reference node
2. Using [[Resistive Circuits#Ohm's Law|Ohm's law]], define a current flowing through each resistor in terms of the defined voltage
3. Apply [[Resistive Circuits#Kirchoff's Current Law (KCL)|KCL]] at one of the two nodes in the circuit 
4. Solve the single KCL equation for *v(t)*. If this value is positive then the reference node is the a lower potential than the other node.
##### Current Division
![[Pasted image 20240603011853.png]]
The goal of this passage is to first find a formula for equivalent parallel resistance, then further find a formula for the current division.
We see that *v(t)* must be the same over the two resistors, and further apply [[#Kirchoff's Current Law (KCL)|KCL]] giving us
$$
\begin{align}
i(t)=i_1(t)+i_2(t)
\end{align}
$$
after applying [[#Ohm's Law]] we can now find an expression for the equivalent resistance
$$
\begin{align}
i(t)=\frac{v(t)}{R_1}+\frac{v(t)}{R_2}\\ \\
i(t)=\left( \frac{1}{R_1}+\frac{1}{R_2}\right)\cdot v(t) \\\\
i(t)=\frac{v(t)}{R_P}, \text{  where  } \frac{1}{R_P}=\frac{1}{R_1}+\frac{1}{R_2}
\end{align}
$$
Using some *algebra* we can then mix everything around
$$
\begin{align}
\frac{1}{R_P}=\frac{1}{R_1}+\frac{1}{R_2} \\\\
1=\frac{R_P}{R_1}+\frac{R_P}{R_2}\\ \\
R_1=R_P+\frac{R_P\cdot R_1}{R_2}\\ \\
R_1\cdot R_2 = R_P\cdot R_2 +R_P\cdot R_1 \\ \\
R_1\cdot R_2 = R_P (R_2 + R_1) \\ \\  
 \frac{R_1\cdot R_2}{R_2 + R_1} = R_P \tag{2.17}
\end{align}
$$
But I digress, we can now use all of this information to find an expression for $i_1(t)$ and $i_2(t)$. 
$$
\begin{align} \\
v(t)=R_P\cdot i(t) \\\\
v(t)=\frac{R_1\cdot R_2}{R_2 + R_1}\cdot i(t) \tag{2.18}\\\\
i_1(t)=\frac{v_1}{R_1} \\ \\
i_1(t)=\frac{i(t)\cdot R_P}{R_1}\\ \\
i_1(t)=\frac{i(t)}{R_1} \frac{R_1\cdot R_2}{R_1 + R_2}\\ \\
i_1(t) = i(t)\cdot\left(\frac{R_2}{R_1+R_2} \right)\tag{2.19}
\end{align}
$$
Following the same steps we can get the expression for $i_2(t)$
$$
\begin{align} \\
i_2(t)=i(t)\cdot \frac{R_1}{R_1+R_2}
\end{align}
$$

##### Multiple Source/Resistor Networks
The goal is once again here to find the simplest possible equivalent circuit to determine the constants of the circuit. Combine sources and resistors.
This chapter further proves that we can find the equivalent resistance of multiple resistors connected in parallel
$$
\begin{align}
\frac{1}{R_P}=\sum_{i=1}^{N} \frac{1}{R_i} \tag {2.23}
\end{align}
$$


## Series and Parallel Resistors
This chapter mostly consists of examples 
##### Problem Solving Strategy
 1. Systematically reduce the resistive network so that the resistance seen by the source is represented by a single resistor. 
 2. Determine the source current for a voltage source or the source voltage if a current source is present.
 3. Expand the network, retracing the simplification steps, and apply Ohm’s law, KVL, KCL, voltage division, and current division to determine all currents and voltages in the network.
## Wye-Delta transformations
![[Pasted image 20240603102313.png]]
We use the terminal points to analyse and find the equivalent resistance
$$
\begin{align}
R_{ab}=R_a+R_b=\frac{R_2(R_1+R_3)}{R_1+R_2+R_3}\\ \\
R_{ab}=R_b+R_c=\frac{R_3(R_1+R_2)}{R_1+R_2+R_3}\tag{2.27}\\ \\
R_{ab}=R_a+R_c=\frac{R_1(R_2+R_3)}{R_1+R_2+R_3}
\end{align}
$$
Solving 2.27 gives us the following sets:
$$
\begin{align}
R_{a}=\frac{(R_1\cdot R_2)}{R_1+R_2+R_3}\\ \\
R_{b}=\frac{(R_2\cdot R_3)}{R_1+R_2+R_3}\tag{2.28}\\ \\
R_{c}=\frac{(R_1\cdot R_3)}{R_1+R_2+R_3}\\ \\
\end{align}
$$
$$
\begin{align}
R_{1}=\frac{R_a\cdot R_b + R_c\cdot R_b+ R_a\cdot R_c}{R_b}\\ \\
R_{2}=\frac{R_a\cdot R_b + R_c\cdot R_b+ R_a\cdot R_c}{R_c}\tag{2.28}\\ \\
R_{3}=\frac{R_a\cdot R_b + R_c\cdot R_b+ R_a\cdot R_c}{R_a}\\ \\
\end{align}
$$
In the case where $R_1=R_2=R_3$ and $R_a=R_b=R_c$ we can reduce these sets to:
$$
\begin{align}
R_Y=\frac{1}{3}R_\Delta \\\\
R_\Delta=3\cdot R_Y 
\end{align}
$$
## Dependent sources
We will for now forgo the problem solving strategy of such circuits as it is mere algebra. We can here note that dependent sources are a model of devices such as [[Bipolar Junction Transistors]], [[Field Effect Transistors]], [[Metal-Oxide-Semiconductor Field-Effect Transistors]], and [[Insulated-gate field-effect transistors]]. :)




