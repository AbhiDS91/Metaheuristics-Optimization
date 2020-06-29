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
### The Partical Swarm Function is defined here.(Figure 6) As you can see I have identified the important variables/parameters that are used for the pso                               function ("pso_algo = algorithm(pso(gen=1200, omega = inertia_factor, eta1= self_confidence, eta2 = swarm_confidence,max_vel=vcoeff,seed=4))" from the pygmo documentation. These are seen in Figure 4 below (omega, eta1, eta2 and max_velocity). I made a connection with the varibles of the true partical swarm equation (inertia factor, self confidence, swarm confidence, maximum velocity and population size ....given by Dr Amir from his lecture notes), Figure 5.
###### Figure 4 - Pygmo Documentation - Parameters Explained
![pygmo](images/pygmo.png)
###### Figure 5 - PSO Function and parameters
![pso](images/pso.png)
###### Figure 6 - 'pso_optimizer' Function defined and Solved
![prob](images/problemdef.png)
### All 5 parameters have 3 values each. A unique set of each variable will be run hence the function will run on 3^5 = 243 times and the best result will be given 

## Optimal Result according to the function for Dimension 50
#### Optimal Interia Factor: 0.5
#### Optimal Self Confidence: 3 
#### Optimal Swarm Confidence: 3
#### Optimal Maximum Partical Velocity: 0.7
#### Optimal Population Size:  100
#### The Optimal Result: 
       [ 97.24993591,  77.0609851 , -19.03114881,  25.42869797,
       -22.90880258,  69.57217578,   5.36971394,  61.4807307 ,
       -21.30069848,  92.34681335, -93.97588123,  90.74598671,
        42.8769803 ,  29.30964632, -10.66954844, -65.07461781,
        67.04941626,  94.01877027, -73.00502032, -49.80219853,
        82.00142505,  35.29318271,  24.63214922,   2.44313748,
       -99.30345093, -54.62233875,  95.69145815,  72.25048082,
       -97.12295526,  -2.84462699, -16.71940688,  54.58048368,
        -2.37049339,   4.51291387,  56.40988582,  18.24586951,
       -74.72144476, -78.05614653,  32.58107758,  99.41862298,
       -30.76381164, -64.78909695, -86.42220775, -38.12082259,
       -33.04804036, -24.76648649,  90.44136625,  43.86410221,
        55.86848707,  23.53173227]
###### Figure 7 -Results for dimension 50
![50](images/results)
#### The Best fitness values is -450

