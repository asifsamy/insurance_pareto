# Insurance Policies - Pareto Analysis

In this anlysis, a dataset of **Insurance Policies** has been visualized by different methodologies of **Tableau Public** such as 
Grouping, Set operations, Quick table calculations, Creating calculated field, Creating some parameter to visualize for 
**Top N Values**, and so on. The dataset has 19 fields/columns and more than 35 thousands records of data. However, the number of 
focused columns were only 5 in this project and those are **ID, Gender, Marital Status, Education, and Car Make**. 
Along with some general visualizations, the main tasks were to visualize **Top N Car Companies** were claimed for insurance and create 
a pareto analysis over the **insurance claimer** based on their **gender**, **marital status**, and **education**.

## General Insights
A general visualization was shown to answer the following questions:
1. People of which marital status submit the most claims?
2. Who submits more claims - married men or married women?
3. What is the percentage difference of claims submitted by separated men against separated women?

![alt text](https://github.com/asifsamy/insurance_pareto/blob/master/images/1_general_insights.JPG "Logo Title Text 1")

The above visualization shows that the single people submit most claims. Between married people male submit most claims. And lastly, 
the percentage difference of claims submitted by separated men against separated women was 5.17%

## Formatting
A formatting was done by using following instructions:
1. Create a Calculated field for [# Claims] as distinct count of policy IDs
2. Build a bar chart for number of claims by level of education and sort descendingly
3. Change the color to "golden" (we are talking about money here after all)
4. Add Labels on the chart and match mark color
5. Remove gridlines and hide field labels for rows

![alt text](https://github.com/asifsamy/insurance_pareto/blob/master/images/2_formatiing.JPG "Logo Title Text 1")

## Top N and Others
A visualization was done for dynamically retrieve **Top N Car Companies** those were claimed for insurance. In order to do that a 
set operation was performed. The following instructions were followed to have this.
1. Sort Car Makes descendingly by the number of Claims submitted
2. Create a Set for Top 20 car makes and add to the Sheet
3. Create a Calculated field that will correspond to the Car Make if it is part of the Top 20, and will have a value 'Others' 
if it is not
4. Make sure that your bar chart is sorted descendingly, but the 'Others' row is placed on the bottom

![alt text](https://github.com/asifsamy/insurance_pareto/blob/master/images/3_top_n.JPG "Logo Title Text 1")

## Pareto Analysis
A **Pareto Analysis** over the **insurance claimer** based on **Customer Segment** (their **gender**, **marital status**, and 
**education**) to visualize what customer segments contribute to 80% (Customizable) of all claims.

A bunch of instructions were followed to perform this:
1. Define a customer segment composition (e.g. Gender-Marital Status-Education) and build a sorted bar chart.
2. Create a calculated field for a running percentage of claims and display it as a line chart.
3. Create a Parameter to give user control over the percentage benchmark of our Pareto analysis (by default -80%).
4. Display the reference line corresponding to the parameter value and find out where 80% of total number of claims is reached 
(what customer segments contribute to 80% of all claims).
5. Distinguish the two groups (within 80% and above 80%) by using color.
6. Change parameter value to see how the graph is changing dynamically.

![alt text](https://github.com/asifsamy/insurance_pareto/blob/master/images/4_pareto.JPG "Logo Title Text 1")

### Live Demo
[Click Here](https://public.tableau.com/app/profile/s.m.asif.al.samy/viz/Insurance-Policies-Pareto-Analysis/Pareto)
