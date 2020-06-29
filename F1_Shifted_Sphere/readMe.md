# F1 Shifted Sphere Function Optimization Using the 'Partical Swarm Optimization' Method

###### Figure 1 - Shifter Sphere Fucntion that will be Optimized
![func](images/fuction_f1.png)


### Because of the Nature of the pygmo package, the only way to optimize the Shifted Sphere function using pso from pygmo is to make a Class. The 3 functions of this class are the primary internal functions that PSO will use when running the 'Shifted Sphere' function. 
#### The Class will contain an '__init__' self function consiting of the parameters 'given_bias' (-450 from the CEC2008 pdf), 'given_bounds' (-100 to 100 from the CEC2008 pdf) and 'given_dimensions' (50 and 500 which are specified in the Assignment guidelines). 
![prop](images/properties.png)
#### Next a 'fitness' function (pygmo package rules, the name of these functions can not be changed) is defined. Here the function takes 'self' and 'x' as parameters and returns the output of the shifted sphere function.
#### Thirdly the 'get_bounds' function is defined which takes self as a parameter and returns the bounds and the dimension specified in the problem. 
