---
tags:
  - Notes
links: "[[Math Lecture 5]]"
creation date: 2024-11-09 15:54
modification date: Saturday 9th November 2024 15:54:48
semester: 3
year: 2024
---


---
# Math Lecture 5 Notes

---



# Complex Numbers

- Complex numbers are used to solve equations of the form $(x^2 = -1)$, where the imaginary unit $(i^2 = -1)$.
- A specific example discussed is the quadratic equation $(z^2 + 2z + 5 = 0)$, showing that it has no real solutions.
- The solution for this equation involves calculating the roots using the formula $(z = -\frac{b \pm \sqrt{b^2 - 4ac}}{2a})$, which is extended to complex solutions when the discriminant is negative.



# Representation of Complex Numbers

- A complex number in Cartesian form is expressed as $(z = x + i \cdot y)$, where $(x)$ is the real part and $(y)$ is the imaginary part.
- The notation for the real and imaginary parts is $(\mathbb{z} = x)$$  and $(Im(z) = y)$.
- The conjugate of a complex number $(z = a + i \cdot b)$ is represented as $(z^{*} = a - i \cdot b)$.



# Operations on Complex Numbers

- **Addition**: Given two complex numbers $(z_1)$ and $(z_2)$, $(z_1 + z_2 = (a + c) + i \cdot (b + d))$.
- **Example**: For $(z_1 = 2 + 2i)$ and $(z_2 = 1 - 2i)$, their sum is $(z_1 + z_2 = 3 + 0i)$.
- **Subtraction**: The difference is $(z_1 - z_2 = (a - c) + i \cdot (b - d))$.
- **Multiplication**: The product is given as $(z_1 \cdot z_2 = (a \cdot c - b \cdot d) + i \cdot (a \cdot d + b \cdot c))$.
- **Division**: The division of complex numbers is conducted using the conjugate to simplify $( \frac{z_1}{z_2})$.



# Graphical Representation

- Complex numbers can be represented in the Argand diagram, where the x-axis represents the real part and the y-axis represents the imaginary part.
- The modulus $( |z| )$ of a complex number is calculated as $(\sqrt{x^2 + y^2})$, and the argument is denoted as $( \theta)$, calculated as $( \tan^{-1}(\frac{y}{x}))$.

```tikz  
\begin{document}  
\begin{tikzpicture}[scale=1]  
% Draw the axes  
\draw[->] (-4,0) -- (4,0) node[right] {Re};  
\draw[->] (0,-4) -- (0,4) node[above] {Im};  
  
% Draw the complex number z  
\def\x{2} % Real part  
\def\y{3} % Imaginary part  
\draw[->, thick] (0,0) -- (\x,\y) node[midway, above right] {$z = x + iy$};  
  
% Draw the modulus |z|  
\draw[dashed] (0,0) -- (\x,0) node[midway, below] {$|z| = \sqrt{x^2 + y^2}$};  
\draw[dashed] (\x,0) -- (\x,\y);  
  
% Draw the angle theta  
\draw[->] (0.5,0) arc[start angle=0, end angle={atan(\y/\x)}, radius=0.5] node[midway, right] {$\theta = \arg(z)$};  
  
% Mark the coordinates  
\fill (\x,\y) circle (2pt) node[above right] {$(x,y)$};  
\fill (\x,0) circle (2pt) node[below right] {$(x,0)$};  
\fill (0,\y) circle (2pt) node[left] {$(0,y)$};  
  
% Add grid  
\draw[very thin, gray] (-4,-4) (4,4);  
\end{tikzpicture}  
\end{document}  
```



# Polar Form of Complex Numbers

- A complex number can also be expressed in polar form as $( z = r(\cos(\theta) + i \sin(\theta)))$ or in exponential form as $( z = re^{i\theta})$.
- **Multiplication in Polar Form**: For $( z_1 = r_1 e^{i\phi_1} )$ and $( z_2 = r_2 e^{i\phi_2})$, the product is $( z_1 z_2 = r_1 r_2 e^{i(\phi_1 + \phi_2)} )$.
- **Division in Polar Form**: Similar rules apply, with $( z_1/z_2 = \frac{r_1}{r_2} e^{i(\phi_1 - \phi_2)} )$.


# De Moivre's Theorem

- The theorem states that $( (r(\cos(\phi) + i \sin(\phi)))^n = r^n (\cos(n\phi) + i \sin(n\phi)) )$.
- Example exploration includes finding roots of complex numbers and applying the formula for multiple solutions.