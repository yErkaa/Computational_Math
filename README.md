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
