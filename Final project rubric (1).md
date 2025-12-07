# DATA2060 Final Project Rubric

### Overview

You will work in teams of 3-4 and implement a machine learning algorithm from scratch in a jupyter notebook that we didn’t implement in the homework assignments. The final product will look like the coding assignments of the homeworks. Your notebook will have three components:

* You’ll explain the math and the numerical algorithms behind your ML model in one or more markdown cells using references and citations.  
* You’ll implement the ML algorithm from scratch using object oriented programming (a class and corresponding methods). Make sure there are \_\_init\_\_, train, predict, loss, etc. methods as required by your algorithm. You can only use python and numpy in this section.  
* You will develop (unit) tests to make sure:   
  * each method of your algorithm works correctly in isolation,   
  * edge cases are handled appropriately,  
  * your implementation can correctly and exactly reproduce results obtained from sklearn.  
  * You can use pandas, matplotlib, sklearn, pytest, and other packages as needed in this section.

Your team’s final report will be the pdf version of the jupyter notebook submitted to Gradescope, and each team will also give a final presentation to describe their algorithm and tests/results to the rest of the class. The slides of the final presentation will also be submitted to gradescope.

### Timeline

We have created [a google sheet](https://docs.google.com/spreadsheets/d/1PVfIAGzW9ndAZJUD4rL0WC6P8H1wLiKCLHU5K2ycfjM/edit?usp=sharing) where you will need to add your team’s name and the ML algorithm your team selects, and links to previous work by October 24th. Students who are not part of a team will be randomly teamed up with other students by the end of October. Some example ML algorithms are described in the next section. Your team can select one of those or look for a different ML algorithm. If you want to work on a different algorithm, at least one member of your team needs to meet with the instructor and get approval by the end of October\! We want to make sure that the algorithm you plan to work on is comparable in complexity to the examples below. For example, linear regression with L1 regularization would be too easy, and implementing a convolutional neural network from scratch might be too difficult compared to the examples below.

Each team will have a mentor TA assigned. Your mentor TA will check in with your team three times during the term and answer any questions you might have. You can also come to the instructor’s office hours for help. Here are the expectations for each of those meetings:

* Week of November 10th: You should complete the markdown section of the report and make sure everyone understands the math and numerical methods behind the algorithm.  
* Before the Thanksgiving Break: You should have some unit tests and at least the train and loss methods completed by this point.  
* By December 5th, the week before the final presentations: All methods and tests are completed and tested, and the report is ready for submission. 

**The final presentations will take place during the week of December 8th.** A signup sheet will be posted on the course forum a couple of weeks ahead of time.   
**The final report needs to be submitted to Gradescope by December 14th.** The final deadline will be posted on the course forum a couple of weeks ahead of time. If you receive any feedback and comments during your final presentation, your team is expected to address those in the final report.

### Example ML algorithms

1. **Gaussian Naive Bayes for classification**

We cover the Naive Bayes algorithm for categorical (binary) features (Chapter 24.0 and 24.1 in the textbook). Gaussian Naive Bayes is an extension of the method to continuous features. You can read more about this algorithm [here](https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.GaussianNB.html#sklearn.naive_bayes.GaussianNB).

2. **CART \- Classification And Regression Tree for regression**

We cover the ID3 tree algorithm in class (Chapter 18). CART is the algorithm implemented in sklearn which is slightly different from ID3. If you choose this project, implement it for a regression problem. Check out the references [here](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeRegressor.html#sklearn.tree.DecisionTreeRegressor).

3. **CART \- Classification And Regression Tree for classification**

Same as above but used for classification. Check out the references [here](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html#sklearn.tree.DecisionTreeClassifier).

4. **Boosting**

AdaBoost is an algorithm we cover in class (Lecture 9\) but it is not implemented in any of the HW assignments. If you liked the algorithm, this is your chance to implement it\! The details of the algorithm are described in Chapter 10 of the textbook.

5. **Multiclass classification**

Implement the one-vs-all and the all-pairs algorithms we covered in Lecture 5 using any of the binary classification models you implemented in the homeworks. Compare and contrast the results. If you choose this method, describe in the signup sheet which binary classification algorithm you plan to use.

### Format requirements for the Final Report (70 points)

Here are the sections we expect to see in your final report:

1. **Overview of \[the name of your ML algorithm\] (20 points)**  
* Give an overview of the algorithm and describe its advantages and disadvantages.  
* Representation: describe how the feature values are converted into a single number prediction.  
* Loss: describe the metric used to measure the difference between the model’s prediction and the target variable.  
* Optimizer: describe the numerical algorithm used to find the model parameters that minimize the loss given a training set.

Use markdown in the jupyter notebook, add equations to explain math, and use pseudo-code to explain how numerical algorithms work. Use citations and references. Use at least 500 words (excluding equations and pseudo-code).

2. **Model (20 points)**

This section is one code cell which contains the class of your ML algorithm and any other helper functions. Add docstrings to each method and function and explain what they do and what the inputs and outputs are. Please add comments to the code as well as needed\! *You can only use python and numpy in this section.*

3. **Check model (20 points)**

This section is a collection of code and markdown cells that contain the unit tests and a demonstration that your implementation can reproduce sklearn results. 

There should be several unit tests. Create at least two or three unit tests per method and make sure that edge cases are properly handled. Explain either as comments or in a markdown cell what the goal of each test is and/or what edge case it tests for.

*Apply your ML algorithm and sklearn’s implementation on a public dataset and compare the results.* Include a markdown cell and describe the work. Demonstrate in a code cell that your implementation can successfully and exactly reproduce the sklearn results. *You can use pandas, matplotlib, sklearn, pytest, and other packages in this section.* Use citations and references.  

4. **Github repo (5 points)**

Create a public Github repo and add the link to the report under the title. You can add the link to the repo to your resume as a class project so make sure it is professional. Here are the minimum requirements:

The first thing people inspect in your repo is the readme file. The readme file should give an overview of the project, it states what python version and package versions were used to develop the code so others can run it locally and reproduce your results (add a yaml file for ease of use), and a list of authors with contact info. There should be a license file to let people know what they can and cannot do with your code. Github offers a couple of license options, check those out and decide what’s best for you. The repository should have the following directory structure:

├── data/  
├── src/  
├── .gitignore  
├── LICENSE  
├── README.md  
├── presentation.pdf  
└── report.pdf

All data files are in /data, and your jupyter notebook should be in /src. Feel free to add other folders like /figures, /results, as required. Additionally, you might want to add the pdf versions of your report and the slides as well. Check out one of [my repos](https://github.com/azsom/ODSC-East-2024-ChatGPT-API) as an example. 

5. **References (5 points)**

Collect all citations you used in the Overview and the Check Model sections. Use the [Harvard citation format](https://www.mendeley.com/guides/harvard-citation-guide/). 

6. **Contributions**

We will send out a google form to everyone where you’ll need to describe your and your teammate’s contributions to the final project. We expect that every team member contributes more or less equally to the final project and each team member is expected to receive the same amount of points. If the contributions indicate that one or more team members didn’t pull their weight, they will receive less points proportional to the effort they put in. 

### Final presentation (15 points)

The final presentations will take place during the week of December 8th. We will send out a sign-up sheet a few weeks in advance with available slots. Each team will have a 20 minute slot (15 minutes to present, 5 minutes for audience questions). Each team member should be the main presenter for 4-5 minutes. The goal of the presentation is to summarize your work for your fellow students. Your target audience has decent coding and math skills but assume that they know nothing about the ML algorithm you selected. Your presentation should have the following sections:

- a title slide (1 point),   
- introduce the math behind your ML algorithm, show equations (4 points),   
- describe the numerical techniques, use pseudo-code, do not show actual code (4 points),   
- walk us through the sklearn results you reproduced using your code (4 points),   
- add a summary slide and let the audience know what was particularly interesting about your ML algorithm and what you found challenging as you implemented it (2 points).

There is no need to describe the unit tests during the final presentation.  
