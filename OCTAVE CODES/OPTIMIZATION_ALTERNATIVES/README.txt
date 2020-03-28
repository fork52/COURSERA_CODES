We can use octave's "fminunc()" optimization algorithm along with the "optimset()" function 
that creates an object containing the options we want to send to "fminunc()".


1) USE THE FOLLOWING COMMANDS TO CREATE an configuration/options variable:
>> options = optimset('GradObj','on','MaxIter',100);

2)Initialize Theta
>> initialTheta = zeros( 2 , 1)
initialTheta =

   0
   0

3) THIS RUNS THE ALGO
>> [optTheta , functionVal ,exitFLag ] = fminunc(@costFunction , intialTheta ,options );