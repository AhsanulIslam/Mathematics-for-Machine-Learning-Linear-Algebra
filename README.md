"# Mathematics-for-Machine-Learning-Linear-Algebra   

1st < week 3 < < Identifying special matrices -< Identifying special matrices.py
Instructions
In this assignment, you shall write a function that will test 
if a 4×4 matrix is singular, i.e. to determine if an inverse 
exists, before calculating it.
You shall use the method of converting a matrix to echelon 
form, and testing if this fails by leaving zeros that can’t 
be removed on the leading diagonal.
Don't worry if you've not coded before, a framework for the 
function has already been written. Look through the code, and 
you'll be instructed where to make changes. We'll do the first 
two rows, and you can use this as a guide to do the last two.
Matrices in Python
In the numpy package in Python, matrices are indexed using 
zero for the top-most column and left-most row. I.e., the 
matrix structure looks like this:
A[0, 0]  A[0, 1]  A[0, 2]  A[0, 3]
A[1, 0]  A[1, 1]  A[1, 2]  A[1, 3]
A[2, 0]  A[2, 1]  A[2, 2]  A[2, 3]
A[3, 0]  A[3, 1]  A[3, 2]  A[3, 3]
You can access the value of each element individually using,
A[n, m]
which will give the n'th row and m'th column (starting with zero). You can also access a whole row at a time using,
A[n]
Which you will see will be useful when calculating linear 
combinations of rows.
A final note - Python is sensitive to indentation. All the 
code you should complete will be at the same level of 
indentation as the instruction comment.




2nd < week 4 < < Gram-Schmidt process -<Gram-Schmidt process.py
Instructions
In this assignment you will write a function to perform the 
Gram-Schmidt procedure, which takes a list of vectors and forms 
an orthonormal basis from this set. As a corollary, the procedure
 allows us to determine the dimension of the space spanned by 
 the basis vectors, which is equal to or less than the space 
 which the vectors sit.
You'll start by completing a function for 4 basis vectors,
 before generalising to when an arbitrary number of vectors 
 are given.
Again, a framework for the function has already been written. 
Look through the code, and you'll be instructed where to make 
changes. We'll do the first two rows, and you can use this as 
a guide to do the last two.
Matrices in Python
Remember the structure for matrices in numpy is,
A[0, 0]  A[0, 1]  A[0, 2]  A[0, 3]
A[1, 0]  A[1, 1]  A[1, 2]  A[1, 3]
A[2, 0]  A[2, 1]  A[2, 2]  A[2, 3]
A[3, 0]  A[3, 1]  A[3, 2]  A[3, 3]
You can access the value of each element individually using,
A[n, m]
You can also access a whole row at a time using,
A[n]
Building on last assignment, in this exercise you will 
need to select whole columns at a time. This can be done with,
A[:, m]
which will select the m'th column (starting at zero).
In this exercise, you will need to take the dot product 
between vectors. This can be done using the @ operator. 
To dot product vectors u and v, use the code,
u @ v
All the code you should complete will be at the same level 
of indentation as the instruction comment.



3rd < week 5 < Reflecting Bear  -<Reflecting Bear.py
Background
Panda Bear is confused. He is trying to work out how things 
should look when reflected in a mirror, but is getting the wrong 
results. In Bear's coordinates, the mirror lies along the first 
axis. But, as is the way with bears, his coordinate system is 
not orthonormal: so what he thinks is the direction 
perpendicular to the mirror isn't actually the direction the 
mirror reflects in. Help Bear write a code that will do his 
matrix calculations properly!
Instructions
In this assignment you will write a Python function 
that will produce a transformation matrix for reflecting 
vectors in an arbitrarily angled mirror.
Building on the last assingment, where you wrote a code 
to construct an orthonormal basis that spans a set of input
 vectors, here you will take a matrix which takes simple form in that basis, and transform it into our starting basis. Recall the from the last video,
\( T = E T_E E^{-1} \)
You will write a function that will construct this matrix. 
This assessment is not conceptually complicated, but will build 
and test your ability to express mathematical ideas in code. 
As such, your final code submission will be relatively short, 
but you will receive less structure on how to write it.
Matrices in Python
For this exercise, we shall make use of the @ operator again. 
Recall from the last exercise, we used this operator to take 
the dot product of vectors. In general the operator will combine 
vectors and/or matrices in the expected linear algebra way, i.e. 
it will be either the vector dot product, matrix multiplication, 
or matrix operation on a vector, depending on it's input. 
For example to calculate the following expressions,
\( a = \mathbf{s}\cdot\mathbf{t} \)
\( \mathbf{s} = A\mathbf{t} \)
\( M = A B \),
One would use the code,
a = s @ t
s = A @ t
M = A @ B
(This is in contrast to the \(*\) operator, which performs element-wise multiplication, or multiplication by a scalar.)
You may need to use some of the following functions:
inv(A)
transpose(A)
gsBasis(A)
These, respectively, take the inverse of a matrix, give the transpose of a matrix, and produce a matrix of orthonormal column vectors given a general matrix of column vectors - i.e. perform the Gram-Schmidt process. This exercise will require you to combine some of these functions.


4th < week 5 < PageRank -<PageRank.py
In this notebook, you'll build on your knowledge of eigenvectors 
and eigenvalues by exploring the PageRank algorithm. 
The notebook is in two parts, the first is a worksheet to get 
you up to speed with how the algorithm works - here we will look 
at a micro-internet with fewer than 10 websites and see what it 
does and what can go wrong. The second is an assessment which 
will test your application of eigentheory to this problem by 
writing code and calculating the page rank of a large network 
representing a sub-section of the internet.
Part 1 - Worksheet
