A recurrence is a rule which relates to finding the next value in a succession, using the previous values.
# Types
There exists various types of recurrence relations, depending on your needs, such as linear homogeneous relations like: $$a_n=c_1a_{n-1}+c_2 a_{n-2}\ldots$$
Or non homogeneous recurrence relations like $$a_n=b+c_1a_{n-1}+c_2 a_{n-2}\ldots$$There are also nonlinear recurrence relations: $$a_n=\sqrt{a_{n-1}+a_{n-2}}$$
# Order
This is the largest distance you have to recurse to get the next term. The order of a recurrence: $$a_n=a_{n-1}+\ldots + a_{n-k}$$is $k$.
# Solving 2nd-Order Homogeneous Linear Recurrence Relations
Given some recurrence relation $a_n=r_1 a_{n-1}+r_2 a_{n-2}$, we can solve it through the characteristic polynomial, which is represented as: $$p(x)=x^2-r_1 x-r_2$$Using the polynomial characteristic you solve for the roots $c_1$ and $c_2$ you get two cases:
## Case 1: Two distinct roots
in this case you solve the equations: $$a_n=u c_1^n + vc_2^n$$
## Case 2: Equal roots
In this case you solve the equations: $$a_n=(u+vn)c^n$$
# Solving Non-Homogeneous Linear Recurrence Relations
Let $a_n=a_{n-1}$