# 1) TSP Djibouti 

## Problem Statement: What is the fastest way to move accross all 38 cities in Djibouti ?

## Simulated Annealing and the Genetic algorithm are compared to see which gives the best fitness 

    Two types of cooling methods were used and compared (Exponential Decay and Arithmatic Decay) for simulated annealing. The best 
    fitness value yielded by the the two cooling methods (for simulated annealing) will be chosen and compared with the 
    best fitness value from the genetic algorithm. 

#####    I used jupyter notebook to run my code. 
 
 
 ### Step 1 - Importing of Relavant packages. MLROSE (important) package was used to call the optimization functions
 ###### Figure 1 - Jupyter Notebook Image of Imports
   ![djibouti](photos/imports.png)
   
   
 ### Step 2 - Data Preparation is done in this step. TSP file stored in a dictonary, then the coordinates stored in a list and then eventually an 'optimization object' is defined               to be used later for different methods/algos  
 ###### Figure 2 - Jupyter Notebook Image of some data preparation lines. 
   ![prep](photos/prep.png)
    
 ### Step 3 - Simmulated Annealing algorithm was run on both the cooling methods, Exponential Decay as well as Arithmatic Decay. Necessary Variables were created and appended in a               list. These include the 'best_fitness'(a value indicating the fitness), 'best_state' (the order in which the city should be traversed in) and the 'fitness_curve'                  (can be plotted) that shows
 ###### Figure 3 - Jyputer Notebook Image of the Simulated Algorithm being run.
   ![sim_code](photos/sim_algo_code.png)
