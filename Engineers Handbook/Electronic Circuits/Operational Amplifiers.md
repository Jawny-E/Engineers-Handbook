---
banner: "![[Op-Amps-950x500.webp]]"
banner_y: 1
---
## What is the Operational Amplifier?
The OP-amp is arguably one of the most important circuit components produced for analog circuit design. They were originally made using vacuum tubes, but are today produced as Integrated Circuits([[IC|ICs]]) using a combination of transistors and resistors. One can now find several high quality op-amps for prices as low as $0.40 on a single IC.
>[!tip] Fun fact
>The [[Transistors|transistor]] was invented in 1947 at Bell Labs

The operational amplifier is named such as its intended purpose was to perform mathematical operations such as: addition, subtraction, differentiation, and integration. 
## Models of Op-Amps
When broken down to it's simplest state an op-amp can simply be regarded as a **really good voltage amplifier**. There is however a wide array of different types of op-amps for many different applications, this fortunately does not change the topology of our model. 
![[What-is-an-operational-amplifier_1_en.png]]
The output ($V_{OUT}$) is controlled by the noninverting- ($V_{IN+}$) and inverting ($V_{IN-}$) input. The relationship can be described mathematically as:
$$
\begin{align} 
V_{OUT}=A_0(V_{IN+}-V_{IN-})\tag{4.1}
\end{align}
$$
here the voltages are measured with respect to ground and $A_0$ is the *gain* of the op-amp. Typical values of $A_0$ range between 10'000 and 1'000'000. To power this amplification we use voltage supplies $V_{CC}$ and $V_{EE}$. $V_{CC}$ is traditionally a positive voltage, whilst $V_{EE}$
is a negative voltage or just ground itself. 
The model we will use for the op-amp is a dependent voltage source that produces $V_0$. 
![[Pasted image 20240614203453.png]]
This ideal op-amp model:
>[!info]This ideal op-amp model:
>$A_0=\infty$,$R_i=\infty$,$R_0=0$
$$
\begin{align}
i_+=i_-=0 \\
v_+=v_-
\tag{4.2}
\end{align}
$$

## Fundamental Circuits
##### Problem Solving Strategy
1. Use the ideal op-amp model
2. Apply nodal analysis to the resulting circuit
3. Solve nodal equations to express the output voltage in terms of the op-amp input signals
##### Non-Inverting op-amp
##### Inverting op-amp
##### Subtracting op-amp
##### Instrumentation amplifier
##### Electronic Ammeter