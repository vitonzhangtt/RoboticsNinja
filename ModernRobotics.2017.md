# Modern Robotics-Mechanics Planning and Control (2017)

## Proposition 3.8.

$`R = \left(\!
      \begin{array} {c}
        {r_{1}}^T \\ 
        {r_{2}}^T \\ 
        {r_{3}}^T \\ 
      \end{array}
      \!\right)
`$

$`R^T = (r_{1}, r_{2}, r_{3})`$

$`R[\omega]R^T`$ is multiplication of matrics. <br>
The matrix $`[\omega]`$ is a $`3 × 3`$ **skew-symmetric matrix** representation of $`\omega`$. <br>
1. According to [Associative Property](https://github.com/vitonzhangtt/LinearAlgebraNinja/blob/main/Addition-and-multiplication-of-matrices.md#associative-property), then $`R[\omega]R^T=R([\omega]R^T)`$
2. According to [Conversion to matrix multiplication](https://en.wikipedia.org/wiki/Cross_product#Conversion_to_matrix_multiplication), $`[\omega]R^T = {\omega} \times {R^T}`$.

After 1 and 2, $`R[\omega]R^T = R({\omega \times {R^T}}) 
  = \left(\!
      \begin{array} {c}
        {r_{1}}^T \\ 
        {r_{2}}^T \\ 
        {r_{3}}^T \\ 
      \end{array}
    \!\right)   
    \begin{pmatrix}
        {\omega \times r_{1}} & {\omega \times r_{2}} & {\omega \times r_{3}} \\
    \end{pmatrix}
  = \begin{bmatrix}
      {{r_{1}}^T}{(\omega \times r_{1})} & {{r_{1}}^T}{(\omega \times r_{2})} & {{r_{1}}^T}{(\omega \times r_{3})} \\
      {{r_{2}}^T}{(\omega \times r_{1})} & {{r_{2}}^T}{(\omega \times r_{2})} & {{r_{2}}^T}{(\omega \times r_{3})} \\
      {{r_{3}}^T}{(\omega \times r_{1})} & {{r_{3}}^T}{(\omega \times r_{2})} & {{r_{3}}^T}{(\omega \times r_{3})} \\
    \end{bmatrix}
`$

## Reference
1. Book: [Modern.Robotics-Mechanics.Planning.and.Control.2017.pdf](https://www.amazon.com/Modern-Robotics-Mechanics-Planning-Control/dp/1107156300)


