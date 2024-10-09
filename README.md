## Lab 1 Report
The algorithms used are stored in the set-cover_gpu.ipynb jupyter notebook.
The configuration (NUM_SETS, UNIVERSE_SIZE, DENSITY) has to be chosen
before launching the program.
I used PyTorch tensor to better the performance when sizes are larger.
When universe size is smaller performance are worse.
In the file choices.txt i stored the choices made by the algorithm for
each configuration. The choice was done launching all my strategies for 
the given configurations, each of them with the same starting solution.
The strategy achieving the best solution was chosen (not really a consistent
way of doing this, should have used Monte Carlo Simulation, but time was 
strict).
So now when notebook is runned the "best" configuration is chosen.
In the plots folder i plotted the history of solution using various algorithm
and configuration, feel free of looking at them.
## Alert
Solution is GPU intensive, if you cant use it try 
set-cover_cpu_NotComplete.ipynb but i warn you that it is a very basic notebook 
and it is much more messy.
## Conclusions
The best performing algorithm depends on the conditions. If we can deeply
explore a local minimum Iterated Local Search and Simulated Annealing works
best. If we cant (not enough steps, not enough computing power/time) a more
exploitative approach works best (Multi_Tweak random selecting a solution
only if it is better in terms of cost).
