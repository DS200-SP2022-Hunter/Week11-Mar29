# Lab Assignment 10, Due on [Canvas](https://psu.instructure.com/courses/2174978/modules/items/35216133), Apr. 6 at 11:59pm
## Implement a Logistic Regression Classifier

The main objective of today's lab is to use the `minimize` function from [Section 15.3](https://inferentialthinking.com/chapters/15/3/Method_of_Least_Squares.html) to train a classifier to predict chronic kidney disease using a logistic regression model.  The dataset comes from [Section 17.1](https://inferentialthinking.com/chapters/17/1/Nearest_Neighbors.html).

**Objective**:  Use the `ckd` dataset from [Section 17.1](https://inferentialthinking.com/chapters/17/1/Nearest_Neighbors.html) to train a classifier to predict chronic kidney disease using a linear function of hemoglobin and white blood cell count.  Because the response variable has values 0 and 1, where 1 is a patient without CKD and 0 is a patient without, we won't minimize the mean of the squared errors as we do for linear regression.  Instead, we will minimize the mean of a special function that makes our procedure logistic regression.

**Your assignment** is as follows:

1. Load the Jupyter notebook for [Section 17.1](https://inferentialthinking.com/chapters/17/1/Nearest_Neighbors.html) of the textbook from GitHub as you've done in the past. You might want to change the `path_data` object so that it points to the URL where the dataset can be found:  `http://personal.psu.edu/drh20/200DS/assets/data/`

2. As in the first block of code in Section 17.1.1, read the dataset from the `ckd.csv` file as a `Table` object and give it the name `ckd`, for chronic kidney disease . 

3. We only need a 3-column subset of this dataset, so (again, as in Section 17.1) rename the `ckd` object as follows:
```
ckd = ckd.select('Class', 'Hemoglobin', 'White Blood Cell Count')
```
4. Produce a scatterplot with hemoglobin on the horizontal axis and white blood cell count on the vertical axis, with the points labeled by color according to their values of `Class` (1 for CKD, 0 for no CKD). Use the last block of code in Section 17.1.1 as a model.

5. On your scatterplot, you should see the 

9. _(Optional, for an extra point):_ The original dataset covers two different races, the First Night 5K and the Arts Festival 5K.  There are 24 people who ran both of them.  Create a new dataset with these 24 people, and give a bootstrapped 95% confidence interval for the mean difference between an individual's First Night finishing time and that individual's Arts Fest finishing time.  As above, discuss which population you think this result might apply to.

10.  Finally, make sure that your Jupyter notebook only includes code and text that is relevant to this assignment.  For instance, if you have been completing this assignment by editing the original code from Section 13.2, make sure to delete the material that isn't relevant before turning in your work.

When you've completed this, you should select "Print" from the File menu, then save to pdf using this option.  The pdf file that you create in this way is the file that you should upload to Canvas for grading.  We have found that if you can select the "A3" paper size from the advanced options, this seems to solve the problems that are sometimes encountered in this step.


