<div align="center">

# Applying-Knowledge-Tracing-Algorithm-to-understand-Behavior
  
[About](#about) •
[Configuration Requirements](#configuration-requirements) •
[Findings](#installation) •
[Further Modifications](#how-to-contribute)  
  
</div>

## 📒 About <a name="about"></a>

Imagine a situation where there is one teacher and say, 25 students in a classroom, it becomes really difficult for the teacher to give individual feedback on every task that is assigned to them. The distribution of teacher’s attention on every single student that is present in the classroom is not even. This leads to only few students gaining the overall benefits of the learning, leading other less attention and feedback given student to have a very poor experience. It is not even the teacher’s fault but human constraints and disability to personalize feedback for every task of every student. This is where data science can come into the picture and could help teachers in giving personalized feedbacks.

The main idea and purpose of this project is to understand behavior of the students in a simulated learning environment and individualize the feedbacks. 

## 👨‍💻 Configuration Requirements <a name="configuration-requirements"></a>

What is the required configuration for running this code
1. OS - Windows 10
2. Python 3.7+
3. Libararies - Pytorch, Sklearn, Matplotlib, ngrams
4. Jupyter Notebook

## 🖥️ Findings <a name="installation"></a>

<img src='https://github.com/saumyagoyal95/Applying-Knowledge-Tracing-Algorithm-to-understand-Behavior/blob/f5e81091873a85e9288e60aa2938db5cff3b9263/Images/EDaParticipant.PNG' width=500px> <br>

The above graph, shows cumulative number of steps (labelled as per the epistemic activity) taken by each participant. 
0 denoting undefined epistemic activity label. From this finding the participants who produced the right diagnosis spent less time on undefined epistemic activity and also less time on EDA-3 i.e Evidence evaluation in comparison to the participants who were mostly wrong.
This can be understood as the participants having better understanding of the problem, spent less time on evaluation as they were able to diagnose the issue with less number of Evidence evaluation step. 

<img src='https://github.com/saumyagoyal95/Applying-Knowledge-Tracing-Algorithm-to-understand-Behavior/blob/f5e81091873a85e9288e60aa2938db5cff3b9263/Images/TimeParticipant.PNG' width=500px> <br>

Comparing the time spent by good (1, 2, 4) and bad (3, 5) performing participants, it was evident that the time taken for solving the problem by good performing participant was less than the time taken by the poor performers. 

<img src='https://github.com/saumyagoyal95/Applying-Knowledge-Tracing-Algorithm-to-understand-Behavior/blob/3e337b9e094af3ad71a6a26c337a31dff22f7bac/Images/CorrelationMatrix.png' width=500px> <br>

- Number of steps in EDA_1 , 2, 3, and 4 i.e. Problem identification, Evidence generation, Evidence evaluation and Hypothesis Generation respectively have positive correlation with EDA_0 i.e. steps not included in the epistemic activities labels. So more the number of steps in EDA 1, 2, 3 and 4, more are the chances of carrying out tasks that are not labelled as per the epistemic activities. And more the number of steps in EDA_0  , less is the correlation with influencing the correct result. This could possibly mean that if more steps are taken in the generation of the result, that means the student is does not know how exactly to diagnose the situation is experimenting, sometimes can reach the right goal and sometimes not.
- Number of steps in EDA_2 i.e. Evidence generation has -0.38 on generating the correct result. So more the steps carried out in the evidence generation can mean that the student is not confident enough with current evidence or does not know which correct evidences need to be generated to proceed further.
-	Number of steps in EDA_1, 2, 3 and 4 i.e. Problem identification, Evidence generation, Evidence evaluation and Hypothesis Generation are highly positively correlate among each other.


<img src='https://github.com/saumyagoyal95/Applying-Knowledge-Tracing-Algorithm-to-understand-Behavior/blob/f5e81091873a85e9288e60aa2938db5cff3b9263/Images/ImportantFactors.PNG' width=500px> <br>

For generalizing, I ignored the case assigned to feature. And made another classifier using only the most influential features EDA 0, 1 and 2 i.e. not defined epistemic activity, Problem Identification and Evidence Generation respectively. The model showed 72.39% on the test data with just the information on the number of steps and time spent on EDA 0, 1 and 2.

<img src='https://github.com/saumyagoyal95/Applying-Knowledge-Tracing-Algorithm-to-understand-Behavior/blob/main/Images/TestDataset.PNG' width=500px> <br>

From the above experiment, it can be concluded that with minimum information of 50-60% which averages to 78-85 steps into the problem solving, where each step is labelled with some epistemic activity, this model can predict with 80 percent of the accuracy whether the student will be able to reach the end result or not. 

This result seems promising as, with the help of this model we can give early feedbacks to the students while they are trying to solve a problem and hence can influence their results in the right direction.


## ✍️ Further Modifications <a name="how-to-contribute"></a>

The current Deep learning model gives feedback by knowing 50-60% of the steps. 

With a different model architecture and more data this can be further reduced with increased accuracy and giving feedback in the constant interval 10-15steps throughout the problem solving procedure. Also, data showcasing after each step which skill is learned could help in potentially collaborating Knowledge tracing with the above mentioned feedback mechanism. This feedback mechanism along with the exact detail on the skills that needs to be brushed up could help in better learning. This can also be integrated in the E-learning platforms and also in the assignments that students do on the weekly basis. Knowing the influence of scaffolding and feedbacks on learning this kind of model could help in individualizing the learning.
