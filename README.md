Part by part explanation for code (Refer to program for numerical labels in the comments)

1.Importing necessary libraries:
  numpy - numerical operations on array
  pandas - handling the csv file
  pathlib.Path - file path handling
  scipy.optimize - provides optimization functions
  time - time measurement

2.Data loading:
  reads the data from the csv file and converts it into two separate arrays and prints the number of elements
  also checks if the file exists

3.Parametric curve function definition:
 defines x(t) and y(t) based on theta,X and M

4.Nearest point search:
  Constructs a grid and finds the nearest point( the point with the minimum distance from the observed point and the curve ) and its index(t).
  The grid based nearest point search is used for its speed of processing and relative accuracy as compared to a gradient based search.

5. Cost function defintion:
   Defines what we are trying to minimize (theta, M, X)
   Checks the bounds and assigns penalties to parameters that don't conform to the constraints

6. Optimizer:
   Differential evolution is used to find a rough global minimum and L-BFGS-B is used to fine tune the algorithm around the minimum and prints the final optimized parameters
   

8. Accuracy:
   Computes the RMS error

8.Saving the results
9.Computing L1 distance
  
