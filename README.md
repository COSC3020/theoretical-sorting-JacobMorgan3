[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/9YUeXH71)
# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

### Method
To verify that this code runs in linear time I would compare its run time (how long it took to sort a list) for a small list of 50 element with it's runtime of a larger list of 500. We could compare the actual run times with the different input sizes and see if they are proportional. We could do this for many input sizes to get an idea of how it preforms. We could also compare it's runtime against other sorting algorithms. Since we know their time complexity and can see their implementation, we could compare the actual run times and see if they difference is proportional and appropriate for the known algorithms complexity and the supposed new algoithms complexity. We would use the same machine for testing. 

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

### Answer
The new algorithm could not be $O(n)$, because the complexity of the sorting problem is $Omega(nlg(n))$. Since this is a sorting problem there are only two possiblities, an element is sorted or it is not sorted, If it is sorted then we do nothing, if it is not sorted then we move it. The algorithm is like a binary tree. Each node is a desicion and the children of a node are the two possiblities. For input $n$ there are $n!$ leaves (properties of binary trees) and the height of the tree is at least $lg(n!)$ In the worse case we would make $lg(n!)$ comparisions, so the problem as a whole has a complexity of $Omega(n*lg(n))$ which is larger than $n$.   

Add your answers to this markdown file.
