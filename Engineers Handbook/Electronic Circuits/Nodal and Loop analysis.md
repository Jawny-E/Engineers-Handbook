---
banner: "![[node-loop.jpg]]"
banner_y: 0.265
---
## Nodal Analysis for an N-node Circuit
1. Determine the number of nodes in the circuit. Select one node as the *reference node*. Assign a node voltage between each nonreference node and the reference node. For an N node circuit, there are N-1 node voltages. As a result, there are N-1 linearly independent equations that you can use to solve for the node voltages
2. Write a constraint equation for each voltage source - independent or dependent- in the circuit in terms of the assigned node voltages using [[Resistive Circuits#Kirchoff's Voltage law (KVL)|KVL]]. Each constraint equation represents one of the necessary linearly independent equations, and $N_v$ linearly independent equations. For each dependent voltage source, express the controlling variable for that source in terms of node voltages. A voltage source may be connected between a non-reference node and the reference node or between to non-reference nodes. A [[#Supernodes|supernode]] is formed by a voltage source and its two connecting nonreference nodes. 
3. Use [[Resistive Circuits#Kirchoff's Current Law (KCL)|KCL]] to formulate the remaining $N-1-N_v$ linearly independent equations. First, apply KCL at each nonreference node not connected to a voltage source. Second, apply KCL at each supernode. Treat dependent current sources like independent current sources when formulating the KCL equations. For each dependent current source, express the controlling variable in terms of the node voltages. 
## Loop Analysis for an N-loop circuit
1. Determine the number of independent loops in the circuit. Assign a **loop current** to each independent loop. For an N-loop circuit, there are N-loop currents. As a result, N linearly independent equations must be written to solve for the loop currents. 
2. If current sources are present in the circuit, two techniques can be employed. In the first case, one loop current is selected to pass through one of the current sources. The remaining loop currents are determined by open-circuiting the current sources in the circuit and using this modified circuit to select them. In the second case, a current is assigned to each mesh in the circuit. 
3. Write a constraint equation for each current source - independent or dependent - in the circuit in terms of the assigned loop currents using KCL. Each constraint equation represents one of he necessary linearly independent equations, and $N_I$ current sources yield $N_I$ linearly independent equations. For each dependent current source, express the controlling variable for that source in terms of the loop currents
4. Use [[Resistive Circuits#Kirchoff's Voltage law (KVL)|KVL]] to formulate the remaining $N-N_I$ linearly independent equations. Treat dependent voltage sources like independent voltage sources when formulating the KVL equations. For each dependent voltage source, express the controlling variable in terms of the loop currents.
## Concepts
#### Supernodes

#### dsafnl