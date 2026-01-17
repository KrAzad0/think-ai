---
layout: post
title: "Canonical Commutation Relations and the Heisenberg Uncertainty Principle"
date: 2026-01-16 02:00:00 +0530
categories: quantum-mechanics
tags: [uncertainty-principle, commutation-relations, quantum-mechanics, wave-functions]
---

In this post, we derive the canonical commutation relations and the Heisenberg uncertainty principle following the elegant approach of Landau and Lifshitz.

## 1. Coordinate Representation and Basic Operators

In the coordinate representation, a quantum state is described by a wavefunction:

$$\psi(\mathbf{r}) = \psi(x, y, z)$$

The coordinate operators act by multiplication:

$$\hat{x}\psi(\mathbf{r}) = x\psi(\mathbf{r}), \quad \hat{y}\psi(\mathbf{r}) = y\psi(\mathbf{r}), \quad \hat{z}\psi(\mathbf{r}) = z\psi(\mathbf{r})$$

The momentum operators act as derivatives:

$$\hat{p}_x = -i\hbar\frac{\partial}{\partial x}, \quad \hat{p}_y = -i\hbar\frac{\partial}{\partial y}, \quad \hat{p}_z = -i\hbar\frac{\partial}{\partial z}$$

## 2. Commutation Rules

### 2.1 Cross Commutators Vanish

For operators corresponding to different axes, the commutators vanish. For example:

$$[\hat{p}_x, \hat{y}] = \hat{p}_x\hat{y} - \hat{y}\hat{p}_x = -i\hbar\frac{\partial}{\partial x}(y\psi) - y\left(-i\hbar\frac{\partial\psi}{\partial x}\right) = 0$$

Similarly:

$$[\hat{p}_x, \hat{z}] = 0, \quad [\hat{p}_y, \hat{x}] = [\hat{p}_y, \hat{z}] = 0, \quad [\hat{p}_z, \hat{x}] = [\hat{p}_z, \hat{y}] = 0$$

### 2.2 Same-Axis Commutator Equals $i\hbar$

For operators on the same axis:

$$[\hat{p}_x, \hat{x}] = \hat{p}_x\hat{x} - \hat{x}\hat{p}_x = -i\hbar\frac{\partial}{\partial x}(x\psi) - x\left(-i\hbar\frac{\partial\psi}{\partial x}\right) = -i\hbar\psi = i\hbar$$

Therefore:

$$[\hat{p}_i, \hat{x}_k] = -i\hbar\delta_{ik}$$

where $\delta_{ik}$ is the Kronecker delta.

## 3. Useful Commutator Identities

### 3.1 Momentum with a Function of Coordinates

For a smooth function $f(\mathbf{r})$:

$$[\hat{p}, f(\mathbf{r})] = -i\hbar\nabla f(\mathbf{r})$$

### 3.2 Coordinate with a Function of Momenta

In momentum representation:

$$[\hat{r}, f(\mathbf{p})] = i\hbar\nabla_p f(\mathbf{p})$$

## 4. Heuristic Uncertainty Estimate via Fourier Reasoning

Suppose a particle is localized in a region of typical sizes $\Delta x, \Delta y, \Delta z$ with mean momentum $\mathbf{p}_0$. We can write:

$$\psi(\mathbf{r}) = u(\mathbf{r})e^{i\mathbf{p}_0\cdot\mathbf{r}/\hbar}$$

where $u(\mathbf{r})$ differs appreciably from zero only inside that region.

The momentum-space amplitude (Fourier transform) is:

$$a(\mathbf{p}) \sim \int_{\mathbb{R}^3} u(\mathbf{r})e^{i(\mathbf{p}_0 - \mathbf{p})\cdot\mathbf{r}/\hbar}d^3r$$

The integral cancels when the phase oscillates rapidly. Thus $a(\mathbf{p})$ is appreciable only when:

$$\frac{(p_x - p_{0x})\Delta x}{\hbar} \sim 1 \quad \Rightarrow \quad \Delta p_x \Delta x \sim \hbar$$

This gives us the order-of-magnitude relation:

$$\Delta p_x \Delta x \gtrsim \hbar, \quad \Delta p_y \Delta y \gtrsim \hbar, \quad \Delta p_z \Delta z \gtrsim \hbar$$

## 5. Exact Heisenberg Inequality in One Dimension

### 5.1 Standard Deviations

Let $\psi(x) \in L^2(\mathbb{R})$ be normalized: $\int |\psi(x)|^2 dx = 1$.

Define expectation values:

$$\langle A \rangle = \int \psi^*(x) \hat{A} \psi(x) dx$$

Define:

$$\langle x \rangle = \int x|\psi(x)|^2 dx, \quad \langle p \rangle = \int \psi^* \left(-i\hbar\frac{d}{dx}\right)\psi dx$$

$$\Delta x^2 = \langle (x - \langle x \rangle)^2 \rangle, \quad \Delta p^2 = \langle (p - \langle p \rangle)^2 \rangle$$

Without loss of generality, assume $\langle x \rangle = 0$ and $\langle p \rangle = 0$ (by shifting origin and multiplying by a plane wave).

Then:

$$\Delta x^2 = \int x^2|\psi|^2 dx$$

$$\Delta p^2 = \hbar^2 \int \left|\frac{d\psi}{dx}\right|^2 dx$$

### 5.2 Key Nonnegativity Inequality

Let $\lambda \in \mathbb{R}$ be arbitrary. Consider:

$$I = \int |x\psi - \lambda\psi'|^2 dx \geq 0$$

Expanding:

$$I = \int x^2|\psi|^2 dx - 2\lambda\Re\int x\psi^*\psi' dx + \lambda^2\int |\psi'|^2 dx$$

Using integration by parts:

$$\int x\psi^*\psi' dx = \frac{1}{2}\int \psi^* d(x^2\psi) = -\frac{1}{2}\int |\psi|^2 dx = -\frac{1}{2}$$

Therefore:

$$I = \Delta x^2 + \lambda + \frac{\lambda^2}{\hbar^2}\Delta p^2 \geq 0$$

This quadratic in $\lambda$ is nonnegative for all real $\lambda$, so its discriminant must satisfy:

$$1 - 4\Delta x^2 \frac{\Delta p^2}{\hbar^2} \leq 0$$

This yields the **Heisenberg uncertainty principle**:

$$\boxed{\Delta x \Delta p \geq \frac{\hbar}{2}}$$

## 6. Minimum-Uncertainty Gaussian Wave Packets

Equality occurs when $I = 0$ for some $\lambda$, i.e., when:

$$x\psi = \lambda\psi'$$

This differential equation gives a Gaussian:

$$\psi(x) = C \exp\left(-\frac{x^2}{4\Delta x^2}\right)$$

Allowing a mean position $x_0$ and mean momentum $p_0$, the normalized form is:

$$\psi(x) = \left(\frac{1}{2\pi\Delta x^2}\right)^{1/4} \exp\left[i\frac{p_0(x-x_0)}{\hbar} - \frac{(x-x_0)^2}{4\Delta x^2}\right]$$

For this state:

$$\Delta p = \frac{\hbar}{2\Delta x} \quad \Rightarrow \quad \Delta x \Delta p = \frac{\hbar}{2}$$

## 7. General Uncertainty Relation from Commutators

For any two Hermitian operators $\hat{f}$ and $\hat{g}$, the Robertson bound states:

$$\Delta f \Delta g \geq \frac{1}{2}|\langle[\hat{f}, \hat{g}]\rangle|$$

If $[\hat{f}, \hat{g}] = ic$ where $c$ is a real constant, then:

$$\Delta f \Delta g \geq \frac{|c|}{2}$$

## 8. Semiclassical Reading and the Poisson Bracket

In semiclassical situations, one replaces:

$$\frac{i}{\hbar}[\hat{f}, \hat{g}] \rightarrow \{f, g\}_{\text{Poisson}}$$

where $\{f, g\}$ is the Poisson bracket.

If $f = H$ (Hamiltonian) and $g$ has no explicit time dependence, classical mechanics gives:

$$\frac{dg}{dt} = \{g, H\}$$

Semiclassically:

$$\Delta E \Delta g \sim \hbar\left|\frac{dg}{dt}\right|$$

---

## Conclusion

The Heisenberg uncertainty principle is a fundamental consequence of the canonical commutation relations in quantum mechanics. It reveals the intrinsic wave-particle duality and sets fundamental limits on the precision with which complementary observables can be simultaneously measured. Gaussian wave packets achieve the minimum uncertainty bound, making them particularly important in quantum optics and quantum information theory.

**References:**
- L.D. Landau and E.M. Lifshitz, *Quantum Mechanics: Non-Relativistic Theory*
- J.J. Sakurai, *Modern Quantum Mechanics*
