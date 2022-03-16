<div align="center">

# Applying-Knowledge-Tracing-Algorithm-to-understand-Behavior
  
[About](#about) •
[Configuration Requirements](#configuration-requirements) •
[Findings](#installation) •
[Further Modifications](#how-to-contribute)  
  
</div>

## 📒 About <a name="about"></a>

Nelson Mandela once said, “Education is the most powerful weapon which you can use to change the world”. But little did we know that pandemic (Covid-19) of this sort will occur having the potential to make our lives come to a standstill. One of the many effects came into the education industry as well. A major shift to the online based learning was seen during this time, thanks to technology we still managed to survive. But there still are feedback gaps in education system that needs to be fulfilled.  As the importance of feedbacks in learning is known to be very effective a little has been done to individualize these feedbacks.

The main idea and purpose of this project is to understand behavior of the students in a simulated learning environment and individualize the feedbacks. 

## 👨‍💻 Configuration Requirements <a name="configuration-requirements"></a>

What is the required configuration for running this code
1. OS - Windows 10
2. Python 3.7+
3. Libararies - Pytorch, Sklearn, Matplotlib, ngrams
4. Jupyter Notebook

## 🖥️ Findings <a name="installation"></a>

<img src='https://github.com/saumyagoyal95/Applying-Knowledge-Tracing-Algorithm-to-understand-Behavior/blob/19e28da9460277e9c39aa486d38624281a9f5b9a/Images/Correlation%20matrix.png#gh-dark-mode-only' width=400px> <br>

<img src='https://github.com/saumyagoyal95/Applying-Knowledge-Tracing-Algorithm-to-understand-Behavior/blob/19e28da9460277e9c39aa486d38624281a9f5b9a/Images/EDA-withEDAsteps.png' width=400px> <br>

(See RNN-mode.ipynb)
From the above experiment, it can be concluded that with minimum information of 50-60% which averages to 78-85 steps into the problem solving, where each step is labelled with some epistemic activity, this model can predict with 80 percent of the accuracy whether the student will be able to reach the end result or not. 

This result seems promising as, with the help of this model we can give early feedbacks to the students while they are trying to solve a problem and hence can influence their results in the right direction.


## ✍️ Further Modifications <a name="how-to-contribute"></a>

The current Deep learning model gives feedback by knowing 50-60% of the steps.  With a different model architecture and more data this can be further reduced with increased accuracy and giving feedback in the constant interval 10-15steps throughout the problem solving procedure. Also, data showcasing after each step which skill is learned could help in potentially collaborating Knowledge tracing with the above mentioned feedback mechanism. This feedback mechanism along with the exact detail on the skills that needs to be brushed up could help in better learning. This can also be integrated in the E-learning platforms and also in the assignments that students do on the weekly basis. Knowing the influence of scaffolding and feedbacks on learning this kind of model could help in individualizing the learning.
