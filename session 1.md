# Install Anaconda
* Install Python for 3.6
This creates a new cond environment  
``conda create --name ml``  
This activates the cond environment you just created  
``activate ml``  
This is the list of packages you need.  
``conda install tensorflow``  
``conda install numpy``  
``conda install keras``  
``conda install jupyter``  
``conda install matplotlib``  
# AI v ML
Artificial Intelligence is the pursuit of creatings programs with the facade (until the robots take over) of real intelligence. The general goal is human level, although some seek to go beyond.
Machine Learning, is the pursuit of artificially intelligent systems using data to learn.
ML is a subset of AI.
Deep Learning is a subset of ML
## Expert Systems
* It was believed that any task could be described as a set of rules, which if followed, could automate the task.
* All mathematical proofs are essentially this, so it makes sense.
* This was a resonable assumption, and remains so today, however the task of creating expert systems did not become cheaper over time.
    * The creation of the set of rules to automate a task did not become easier as researechers interviewed more and more experts.
* Experts are not always able to explain what it is that they do.
# Machine Learning
Instead of humans encoding rules from experts, an algorithm encodes rules from data. The data often comes from experts. This way we can encode intuitive, and subconscious rules, and often perform better than experts.
Same goal as experts, different routes. Everything is math.
1. ***Supervised Learning***
    * Self Supervised
    * Semi Supervised
2. **Unsupervised Learning**
5. **Reinforcement Learning**
# Statistical Learning (Supervised)
Statistical Learning is the set of tools and techniques to predict with, and understand complex datasets.

Put plainly statistical learning attempts to find the mathematical relationship between a set of inputs and a set of outputs, which it can later use to predict unseen inputs, generate examples of inputs, analyze relationships, etc...

Candidate definition 1: Given a set of data  **X** = {x1, x2, .., xn}, and **Y** = {y1, y2, .., yk} where yi correctly labels xi find some function f, such that f(x) = y for every (x,y)
The kinds of data you have to learn with is called your **features**.
**X** may be multidimensional. xi = (xi1, xi2, xi3) meas you have 3 features.
* English: Given a set X consisting of values x1, x2, .., xn and a set of labels Y consisting of y1, y2, ..., yk our goal is to find a function f that consistely maps xi to yi
* Example: X = {img1, img2, img3, .., imgn} is a set of images of cats and dogs. Y = {C, C, D, C, D, ..., C, D}. We have a set of images of cats and dogs, and a correct label for each image. Our goal is to find a function f which will correctly label imgi with C if imgi is an image of a cat, and D otherwise
***
### Assumptions:
1. There exists a relationship from x to y.
    * We can use ML to determine this!
    *  Statistical learning will not help you classify cats and dogs if all you have is images of whales.
    *  This is called predictive power
2. The functional relationship from x to y
    * We have to the power of the polynomial from x to y
      * linearly: f(x) = ax + b
      * Power of 2: f(x) =a x^2 + bx + c
      * Power of 3: f(x) = ax^3 + bx^2 + cx + d
***
## Bias
Statistical learning techniques will learn from the data you give it, and will be affected the quality. If we have 10,000 images of cats and 10,000 images of dogs, where 80% of the images of dogs are golden retrievers, your statistical model **will** learn that being golden is integral to being a dog and not being a cat. This is obviously not true. The relationship in the data was learned, however the relationship contained some unimportant facts. This is called overfitting.

If your data is 99% class A, your model will likely guess class A 100% of the time.
***
#### Examples of statistical learning problems:
Your boss gives you the amount of money the company spent on advertising in newspapers and asks you to predict next month's sales.
* features: The amount of money spent on advertising data
  * Each xi is 1-dimensional
* labels: Next month's sales
* predictive power: Absolutely

Your boss gives you the amount of money the company spent on advertising in newspapers, along with the amount of money the company spent advertising on the internet, and asks you to predict next month's sales.
* features: The amount of money spent on advertising data and the amount of money spent advertising on the web.
  * Each xi is 2 dimensional
* labels: Next month's sales
* predictive power: Absolutely

Your boss gives you the amount of money the company spent on lunch, and asks you to predict next month's sales.
* features: The amount of money the company spent on lunch
* labels: Next month's sales
* predictive power: No
***
## Neural Networks
Neural networks learn features, and then perform predictions on them.
A statistical learning model that can learn extremely complex relationships.
The process for using a neural network is given below:
Essentially a "solve for v" problem, where v is a matrix.
