# Definition
$X$ is exponential if
$$
f(x) = \begin{cases}
\lambda e^{-\lambda x} && x\geq 0 \\
0 && x<0
\end{cases}
$$

# Notation
$$
\exp(\lambda)
$$
# [[Expected Value]]
$$
\mathbb{E}X = \int_{0}^{\infty} x \cdot \lambda e^{-\lambda x}dx = \frac{1}{\lambda}
$$

# [[Moment Generating Function]]
$$
Ee^{tx} = \int_{0}^{\infty}e^{tx}\lambda e^{-\lambda x}dx = \begin{cases}
\text{not defined} && (t\geq \lambda) \\
\frac{\lambda}{\lambda-t} && (t<\lambda)
\end{cases}
$$
# Fact
## **Memoryless** property
#important 
$$
P(X \geq t+s|x\geq t) = P(X\geq s)
$$
- a *conditional* property
here, $x\geq t$ is a *memory*, which we forget.
we only focus on a gap $s$ here.

### proof
$$
\frac{P(X\geq t+s)}{P(X\geq t)} = \frac{\int_{t+s}^{\infty}\lambda e^{-\lambda x}dx}{\int_{t}^{\infty}\lambda e^{-\lambda x}dx} = e^{-\lambda s}
$$

## Constant multiplication
$$
X_{i} \exp(\lambda) \Rightarrow cX_{i} \exp\left( \frac{\lambda}{c} \right) (\forall c>0)
$$
### proof (using [[Moment Generating Function|MGF]])
$$
Ee^{t \cdot cx} = \frac{\lambda}{\lambda-ct} = \frac{\frac{\lambda}{c}}{\frac{\lambda}{c} - t}
$$
