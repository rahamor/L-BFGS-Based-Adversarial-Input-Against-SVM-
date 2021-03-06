# L-BFGS-Based-Adversarial-Input-Against-SVM-

# Data Source
For data, we will use the classic MNIST data set used to recognize hand-written digits. The dataset was originally produced in the 1980s and is now widely-used in machine learning classes as a simple image classification problem.

And this is the source for our MNIST data set.

http://yann.lecun.com/exdb/mnist/

# Method
## L-BFGS
L-BFGS method is developed from Newton's method. Compared with Newton's method, L-BFGS optimization achieves resource-efficient in both computation and storage.
Please check the report for more details.

# Parameters
There are three parameters are subject to change:
## x 
The target picture of a number to be attacked

eg.

x = 3

### <img src="https://user-images.githubusercontent.com/2645110/34134759-aa78a5c6-e42a-11e7-8ecf-1efac9b06e42.png" width="50" height="50" />

## y_prime
The target label 

eg.

y_prime = [1,2,3,4,5,6,7,8,9]

## <img src="https://user-images.githubusercontent.com/2645110/34136543-61eee126-e434-11e7-95c3-48c24471c4ea.png" width="30" height="30" />
The perturbations degree of the attack

if <img src="https://user-images.githubusercontent.com/2645110/34136543-61eee126-e434-11e7-95c3-48c24471c4ea.png" width="20" height="20" /> is too high, the perturbations may be too little to success

if <img src="https://user-images.githubusercontent.com/2645110/34136543-61eee126-e434-11e7-95c3-48c24471c4ea.png" width="20" height="20" /> is too low, the perturbations may be too high to generate the attack target label

eg.

<img src="https://user-images.githubusercontent.com/2645110/34136543-61eee126-e434-11e7-95c3-48c24471c4ea.png" width="20" height="20" /> is usually between 0.001 to 1, the optimal start value would be 0.01

# Result 
For example, this picture shows an successful adversarial attack to mislead the system to predict 3 as 5

the left picture is original, 

the mid picture is the perturbation we add for adversarial attack, 

the right picture is the output

<img src="https://user-images.githubusercontent.com/2645110/34134760-aa82300a-e42a-11e7-81a1-54e86d21b59e.png" width="200" height="100" /> 

The picture below is an successful result for attacking image 5 to label 4,6,8

<img src="https://user-images.githubusercontent.com/2645110/34134983-e7f44544-e42b-11e7-9e7d-c678701b91fa.png" width="200" height="200" /> 

# Conclusion
The following link is the report of this project.

[Report](https://github.com/sunyi199374/L-BFGS-Based-Adversarial-Input-Against-SVM-/blob/master/L-BFGS-Based-Adversarial-Input-Against-SVM.pdf)
