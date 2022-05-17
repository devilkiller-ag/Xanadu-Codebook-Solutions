<a href="https://pennylane.ai/"><img src="/assets/pennylane_thin.png"></a>
# Xanadu Codebook Solutions

This repository contains solutions to codercises of [Xanadu Codebook](https://codebook.xanadu.ai/) for Learning Quantum Computing using cross-platform python library for differential programming of quantum computers - [Pennylane](https://pennylane.ai/).

<!-- Read this in other languages:  -->

<img src="https://img.icons8.com/external-xnimrodx-lineal-gradient-xnimrodx/64/000000/external-alert-notification-xnimrodx-lineal-gradient-xnimrodx-10.png" width=25> Note that this project is meant to be used for **learning** and **researching** purpose only, and it is not meant to be used for production.

## Codercise List

### [I.1](https://codebook.xanadu.ai/I.1) - All about qubits 
1. [Codercise I.1.1.](https://github.com/devilkiller-ag/Xanadu-Codebook-Solutions/blob/main/solutions/I1-01-NormalizeTheQuantumState.ipynb) Suppose we are given an unnormalized quantum state |ψ⟩ = α|0⟩ + β|1⟩, |α|<sup>2</sup> + |β|<sup>2</sup> ≠ 1. We can turn this into an equivalent, valid quantum state by normalizing it. Write a function that, given α and β, normalizes this state to |ψ′⟩ = α′|0⟩ + β′|1⟩, |α′|<sup>2</sup> + |β′|<sup>2</sup> = 1.
2. [Codercise I.1.2.](https://github.com/devilkiller-ag/Xanadu-Codebook-Solutions/blob/main/solutions/I1-02-InnerProduct.ipynb) Write a function to compute the inner product between two arbitrary states. Then, use it to verify that |0⟩ and |1⟩ form an orthonormal basis, i.e The states are normalized and orthogonal.
3. [Codercise I.1.3.](https://github.com/devilkiller-ag/Xanadu-Codebook-Solutions/blob/main/solutions/I1-03-SimulateMeasureState.ipynb) The function below takes a quantum state vector as input. Complete the function to simulate the outcomes of an arbitrary number of quantum measurements, i.e., return a list of samples 0 or 1 based on the probabilities given by the input state.
4. [Codercise I.1.4.](https://github.com/devilkiller-ag/Xanadu-Codebook-Solutions/blob/main/solutions/I1-04-ApplyU.ipynb) Complete the function below to apply the provided quantum operation U to an input state.
5. [Codercise I.1.5.](https://github.com/devilkiller-ag/Xanadu-Codebook-Solutions/blob/main/solutions/I1-05-SimulateQuantumAlgo.ipynb) Use the functions below to simulate a quantum algorithm that does the following:

  - Initialize a qubit in state |0⟩
  - Apply the provided operation U
  - Simulate measuring the output state 100 times

### [I.2](https://codebook.xanadu.ai/I.2) - Quantum Circuits
1. [Codercise I.2.1.](https://github.com/devilkiller-ag/Xanadu-Codebook-Solutions/blob/main/solutions/I2-01-QuantumCircuit1.ipynb) The code below is a quantum function with all the gates from the above circuit (which we reproduce here for convenience). However, the gates are out of order! Rearrange the lines of the function to match the order of operations in the circuit.
<img src="https://codebook.xanadu.ai/pics/circuit_i-2-1.svg"/>

2. [Codercise I.2.2.](https://github.com/devilkiller-ag/Xanadu-Codebook-Solutions/blob/main/solutions/I2-02-QuantumCircuit2.ipynb) Complete the quantum function in the PennyLane code below to implement the following quantum circuit. We'll then construct a QNode, and run the circuit on the provided device.
<img src="https://codebook.xanadu.ai/pics/circuit_i-2-2.svg"/>

3. [Codercise I.2.3.](https://github.com/devilkiller-ag/Xanadu-Codebook-Solutions/blob/main/solutions/I2-03-QuantumCircuit3.ipynb) The quantum function below implements the circuit from the previous exercise. Apply a decorator to the quantum function to construct a QNode, then run it using the provided input parameters.

4. [Codercise I.2.4.](https://github.com/devilkiller-ag/Xanadu-Codebook-Solutions/blob/main/solutions/I2-04-CircuitDepth.ipynb) What is the depth of the circuit in the picture below?
<img src="https://codebook.xanadu.ai/pics/circuit_i-2-2.svg"/>

### [I.3](https://codebook.xanadu.ai/I.3) - Unitary Matrices
1. [Codercise I.3.1.](https://github.com/devilkiller-ag/Xanadu-Codebook-Solutions/blob/main/solutions/I3-01-UnitaryOperation.ipynb) Complete the quantum function below to create a circuit that applies U to the qubit and returns its state. (Compare this to the earlier function apply_u that you wrote - isn't it nice to not have to worry about the matrix arithmetic?)
2. [Codercise I.3.2.](https://github.com/devilkiller-ag/Xanadu-Codebook-Solutions/blob/main/solutions/I3-02-RotationOperation.ipynb) Apply the Rot operation to a qubit using the input parameters. Then, complete the QNode to return the quantum state vector, using qml.state().

### [I.4](https://codebook.xanadu.ai/I.4) - X and H
1. [Codercise I.4.1.](https://github.com/devilkiller-ag/Xanadu-Codebook-Solutions/blob/main/solutions/I4-01-FlipingBits.ipynb) A common use of the X gate is in initializing the state of a qubit at the beginning of an algorithm. Quite often, we would like our qubits to start in state |0⟩ (which is the default in PennyLane), however there are many cases where we instead would like to start from |1⟩. Complete the function below by using qml.PauliX to initialize the qubit's state to |0⟩ or |1⟩ based on an input flag. Then, use qml.QubitUnitary to apply the provided U.
2. [Codercise I.4.2.](https://github.com/devilkiller-ag/Xanadu-Codebook-Solutions/blob/main/solutions/I4-02-Hadamard.ipynb) What do you think is meant by uniform superposition? Let's explore this using PennyLane. Complete the quantum function below such that it:

  - applies a Hadamard gate to the qubit,
  - returns the state of the qubit with qml.state.
3. [Codercise I.4.3.](https://github.com/devilkiller-ag/Xanadu-Codebook-Solutions/blob/main/solutions/I4-03-HadamardToAll.ipynb) Combining your code from codercises I.4.1, and I.4.2, apply the Hadamard gate to both |0⟩ and |1⟩. What do the two different output states look like? Do you notice anything special about them?
4. [Codercise I.4.4.](https://github.com/devilkiller-ag/Xanadu-Codebook-Solutions/blob/main/solutions/I4-04-HXH.ipynb) Now let's combine what we've just learned. Create a device with one qubit. Then, write a QNode (from scratch!) that applies the following circuit and returns the state. Determine its effect on the two basis states. What do you think this operation does?
<img src="https://codebook.xanadu.ai/pics/hxh.svg"/>
