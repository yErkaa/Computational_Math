Task 1
![image](https://github.com/user-attachments/assets/c3c115e7-227c-4795-adae-9babfe8974fc)
![image](https://github.com/user-attachments/assets/2ea6c861-fe45-4667-a665-11df5af75c7f)

Result:

![image](https://github.com/user-attachments/assets/979f163e-d8d5-4933-a05e-601a042c3fbd)


Explanation:
Define the coefficient matrix A and right-hand side vector b.

Initialize an initial guess vector x as [0, 0, 0].

Check diagonal dominance by ensuring that the absolute value of each diagonal element is greater than the sum of the absolute values of all other elements in the same row.

Perform iterative updates using the Jacobi formula. 

Stop the iterations when the difference between successive approximations (measured by the infinity norm) is less than the tolerance (10^-5).

Print the results of each iteration for clarity.

I use Jacobi method because:
It is an iterative approach suitable for large systems where direct methods (like Gaussian elimination) are computationally expensive.
It relies on successive approximations, making it easier to implement for sparse systems.

Task 2

![image](https://github.com/user-attachments/assets/0d968ef1-3731-438c-8c83-0e2b0ed34503)

![image](https://github.com/user-attachments/assets/a3f9dc97-7e21-41d6-ab6a-82d2b82cb846)

Result:
![image](https://github.com/user-attachments/assets/a3f8b928-9209-432d-86f1-26756e45a2ec)

Explanation:
Define the coefficient matrix A and vector b.

Use partial pivoting.

For each column, find the row with the largest absolute value in the current column.

Swap rows to place this element as the pivot.

Perform forward elimination.
Subtract multiples of the pivot row from rows below it to create zeros below the pivot.

Perform back substitution.
Solve for the variables starting from the bottom row of the upper triangular matrix.

After forward elimination, the matrix is transformed into an upper triangular form where all elements below the diagonal are zero.
This simplifies solving the system through back substitution.

Pivoting reduces the effect of numerical errors and ensures accurate results, especially for systems with large coefficient differences.


I use pivoting because:
Without pivoting, very small or zero pivot elements can lead to division errors or significant rounding errors in floating-point arithmetic.
Pivoting ensures better numerical accuracy and stability.


Task 3:
![image](https://github.com/user-attachments/assets/7a822abc-32fd-42bc-b2f9-5abed9e6677d)

Result:
![image](https://github.com/user-attachments/assets/89042285-82bc-4fed-b1a4-c4417b238d33)


Explanation:
Define the coefficient matrix A and vector b.

Form the augmented matrix by appending b to A.

For each row, normalize the diagonal element to 1 by dividing the row by the diagonal element.

Eliminate all other elements in the column by subtracting appropriate multiples of the current row from other rows.

Directly gives the solution without back substitution.

More systematic and suitable for finding the inverse of a matrix, as the same operations can transform the identity matrix into the inverse.

The diagonal matrix clearly shows the simplified system.

The method is more computationally expensive but systematic.

I use Gauss-Jordan because:
Unlike Gaussian elimination, Gauss-Jordan eliminates the need for back substitution.

It directly reduces the system to a diagonal form (or reduced row-echelon form).

Task 4
![image](https://github.com/user-attachments/assets/dda275d1-3104-42b3-af95-87c22ebce2b0)
![image](https://github.com/user-attachments/assets/c38bad5d-7c53-413e-994d-40b65088f1b3)

Result:
![image](https://github.com/user-attachments/assets/11d74e67-427f-46f9-8cce-8f1b18437814)

Explanation:
Define the coefficient matrix A and vector b.

Initialize an initial guess vector x.

Iteratively update each variable using.

Store the values of all variables at each iteration for table output.

Stop when the difference between successive approximations is below the tolerance.

A smaller tolerance (10^-5 ) increases the number of iterations but ensures higher accuracy.

Larger tolerances lead to faster convergence but lower precision.
Outcome.

I use Gauss-Seidel because:
It is faster than the Jacobi method because it uses the latest updated values immediately within the same iteration.

Suitable for diagonally dominant or symmetric positive-definite matrices.


Task 5
![image](https://github.com/user-attachments/assets/2c9f2694-0263-41a0-a26f-9e28f6a992d9)
![image](https://github.com/user-attachments/assets/84a3b235-e2da-4029-a740-a700ae6725cc)

Result:
![image](https://github.com/user-attachments/assets/b6d44904-9a28-46fa-8296-f5ec6d8151ad)

Explanation:
Solve the system iteratively using the relaxation formula.

Test for 𝜔 = 1.1 (slight acceleration) and ω=1.5 (higher acceleration).

Measure the number of iterations and execution time for each ω.

Lower ω values may converge more slowly.

Higher ω values may lead to divergence if too large.

Solutions, iteration counts, and execution times are compared for both ω.

I use Relaxation because:

Relaxation accelerates convergence by introducing a weighted average of the current and previous values.

Optimal ω values lead to faster convergence.

Task 6
![image](https://github.com/user-attachments/assets/fbf2cf19-19e1-43e5-9e7e-c10fad5b7663)

Result:
![image](https://github.com/user-attachments/assets/87a8b9b2-2fa9-4142-8e4b-9d7fac09ce27)

Explanation:
Solve analytically using the determinant and substitution formulas.

Solve numerically using NumPy’s linalg.solve.

Introduce small perturbations in the coefficients and observe the significant changes in the solution.

Analytical and numerical solutions match for the original system.

A small change in coefficients leads to drastically different solutions, illustrating the instability of ill-conditioned systems.
