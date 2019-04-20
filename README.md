Implement a deep neural network in python from scratch that does images classification.

it is implemented in a series functions:
All the model training take place inside L_layer_model.
inside, initialize_parameters is called first, in which parameters are randomly initialized for the L-layered neural network
Following is a loop for num_iterations.  in the loop, L_model_forward is called,
then compute_cost, then L_model_backward.
Inside L_model_forward is the implementation of forward propagation for the 
[LINEAR->RELU]*(L-1)->LINEAR->SIGMOID computation, where L is the number of layers.
compute_cost compute the cross-entropy J using the following formula:
−1/m * ∑i=1 to m (y(i)log(a[L](i))+(1−y(i))log(1−a[L](i)))
then L_model_backward perform back propagation.  
both L_model_backward and L_model_forward contains numeral helper functions that
compute the linear portion and activation part of the forward and backward prop 
for each layer and then looped for L layers times.
and lastly gradient descent is used to update the parameters of the model.

So to use the model, initialize layers_dims first, with the number of units
in each layer as element. for example, layers_dims = [1000, 300, 200, 5, 1] 
means you want to create a fully connected neural network with a input layer of
1000 units, 3 hidden layer, first with 300, second with 200 and last with 5 units,
and an output with value of 1 or 0.
Then call L_layer_model with X matrix (independent variables) as first parameter,
y (lables) as second, training iterations as third, and whether you want cost at
each iteration print out or not.

The prediction acuracy using this implementation on the dataset i used is 99% on
training sets and 80% on test sets, which is not good, but the whole point of
this exercise is just to fully understand what is implementation detail in the
deep neural network.