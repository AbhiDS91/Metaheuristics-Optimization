# F1 Shifted Sphere Function Optimization Using the 'Partical Swarm Optimization' Method


## Introduction and Setup
###### Figure 1 - Shifter Sphere Fucntion that will be Optimized
![func](images/fuction_f1.png)


### Because of the Nature of the pygmo package, the only way to optimize the Shifted Sphere function using pso from pygmo is to make a Class. The 3 functions of this class are the primary internal functions that PSO will use when running the 'Shifted Sphere' function. 
###### Figure 2 - Class definition
![class](images/classfunc.png)
#### The Class will contain an '__init__' self function consiting of the parameters 'given_bias' (-450 from the CEC2008 pdf), 'given_bounds' (-100 to 100 from the CEC2008 pdf) and 'given_dimensions' (50 and 500 which are specified in the Assignment guidelines). 
###### Figure 3 - Parameters
![prop](images/properties.png)
#### Next a 'fitness' function (pygmo package rules, the name of these functions can not be changed) is defined. Here the function takes 'self' and 'x' as parameters and returns the output of the shifted sphere function.
#### Thirdly the 'get_bounds' function is defined which takes self as a parameter and returns the bounds and the dimension specified in the problem. 

## Problem Definition 
### The Partical Swarm Function is defined here.(Figure 6) As you can see I have identified the important variables/parameters that are used for the pso                               function ("pso_algo = algorithm(pso(gen=1200, omega = inertia_factor, eta1= self_confidence, eta2 = swarm_confidence,max_vel=vcoeff,seed=4))" from the pygmo documentation. These are seen in Figure 4 below (omega, eta1, eta2 and max_velocity). I made a connection with the varibles of the true partical swarm equation (given by Dr Amir from his lecture notes), Figure 5.
###### Figure 4 - Pygmo Documentation - Parameters Explained
![pygmo](images/pygmo.png)
###### Figure 5 - PSO Function and parameters
![pso](images/pso.png)
###### Figure 6 - 'pso_optimizer' Function defined and Solved
![prob](images/problemdef.png)
