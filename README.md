# QuantumStatePreparation
Uses Qiskit to prepare a given quantum state by taking a $2^n$ dimensional vector $\ket{\psi}\in\mathbb{C}^{2^n}$ such that $||\psi||_2=1$, and outputting a circuit $U$ such that:

$$U\ket{0}_n = \sum_{x=0}^{2^n-1}\psi_x\ket{x}_n$$

It does this by iteratively building states:

$$\ket{\psi} = \sum_{x\in\mathbb{F_2^n}}\psi_{x0}\ket{x}_{n-1}\ket{0} + \psi_{x1}\ket{x}_{n-1}\ket{1}$$

In order to prepare state $\ket{\psi}\_{n}$, we first prepare states $\ket{\psi}\_{n-1}$, $\ket{\psi}\_{n-2}$, $\dots$, $\ket{\psi}_{1}$.

The code consists of one main function _make\_circuit_, that takes an input vector $\ket{\psi}\in\mathbb{C}^{2^n}$ and outputs the respective circuit $U_{circ}$.
