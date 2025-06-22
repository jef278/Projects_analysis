# Projects_analysis

## 1 Image analysis 2p or not 2p?
Written for GoogleCoLab - Remember to save model after training. Training and validation sets currently set at 20% validation : 80% training. 

What's the difference 2p or not 2p? Upload an image and the model can give an output of whether or not it's 2p

![image](https://github.com/user-attachments/assets/db3e387b-c706-451b-966e-f9eba38899ca)


## 2 Straight FCS fitting method
Old school FCS analysis, model contains parameters for triplet quenching, 1-3 species present. Applying Stokes-Einstein model and assuming spherical particles.

![image](https://github.com/user-attachments/assets/00c0452e-21b7-4cfe-96da-cef06a5839c0)

For the test data use a fixed K2 of 121

![image](https://github.com/user-attachments/assets/ba2f4919-21d8-4f81-9ff2-d5ffd1c32d7f)


## 3 MEMFCS - using maximum entropy methods for fitting
Adaptation of Maiti et al (Sengupta et al 2009) using python. Use modelling function to check the validity. In principle the model is available if you can find a DOS computer or on Mathematica. This version is adapted for Python.

According to MEM a discrete distribution for τD is the least acceptable solution for noisy data because S is the lowest for such a distribution. The algorithm used in this study begins with equal values for all αi
at all τDi. The distribution is improved in successive iterations: αi(new)=αi(old)+xΔαi. The correction factor xΔαi (an n-dimensional vector) is determined by the optimisation procedure that uses three search directions
constructed using the derivatives, ∇χ2, ∇S and ∇∇χ2. The procedure ensures that χ2 is minimised in successive iterations and S is maximised for that χ2.

The multiplication factor x is determined by the ‘α-chop’ and ‘p-chop’ technique (Skilling and Bryan, 1984) to achieve an aimed value of χ2. Care is taken to avoid negative values for αi, by using only a fraction of x and by equating
negative values to zero. Successive iterations give distributions with reduced χ2. The analysis is terminated when χ2 does not change in successive iterations.

![image](https://github.com/user-attachments/assets/29b44984-281d-434b-a03a-6ad54e592943)

MEMFCS analysis of B2M aggregation kinetics - quiescent growth in low salt pH 2.5 buffer at 37°C
