Code for the computation of the algebraic Thomas decomposition of the symmetrized phase-distribution inverse problem  (maple worksheet "ThomasDecompositionSymmetrizedSystems.mw") with Maple

To run the algebraic Thomas decomposition and your code copy the files "AlgebraicThomas.lib", "AlgebraicThomas.ind" and "ThomasDecompositionSymmetrizedSystems.mw" in a directory of your choice. 

Open "ThomasDecompositionSymmetrizedSystems.mw" with Maple and update the first line of "ThomasDecompositionSymmetrizedSystems.mw", that is the command "libname := "/home/yourdirectory", libname" with the directory in which you copied the files. 

Now you are able to run the code.

The code is divided into two sections:

In the first section we compute an algebraic Thomas decomposition for the models 2,3,4,8 and 9 with respect to the ranking k1>k2>k3>k4>k5>L1>L2>L3>S1>S2. 

A decomposition into simple systems is returned and printed out (also the number of simple systems and the first simple system). 

For each model the list "SystemModelX" contains the symmetrized system for model X and "ResModelX" contains the algebraic Thomas decomposition of "SystemModelX", that is the simple systems defining the decomposition w.r.t the ranking k1>k2>k3>k4>k5>L1>L2>L3>S1>S2.

In the second section we compute algebraic Thomas decompositions for the models 2,3,4,8 and 9 with respect to different rankings (run time for each model less than 2 minutes). 

More precisely, we consider rankings where we permute the ranking on variables k1,k2,k3,k4,k5 and don't change the order of the variables L1>L2>L3>S1>S2. 

We then choose a decomposition with "small" output. The list "permutations" contains all permutations of the set {1,2,3,4,5}. 

Now for each permutation pi we compute an algebraic Thomas decomposition with respect to the ranking pi(k1)>pi(k2)>pi(k3)>pi(k4)>pi(k5)>L1>L2>L3>S1>S2 and save in the list "DataOfSystems" the permutation pi, 

that is the position of the permutation in the list "permutations", the number of simple systems defining the Thomas decomposition for the permuted ranking and the length in digits of the first simple system. We sort the list "DataOfSystems" and choose an entry, 

that is a ranking, which returns a "small" result. We recompute the algebraic Thomas decomposition in "ResModelX" with respect to the chosen ranking and solve in case of model 4, 8 and 9 the quadratic equations. 

The algebraic Thomas decompositions used in the paper "Identifying Markov chain models from time-to-event data: an algebraic approach" are the ones computed in this section.
