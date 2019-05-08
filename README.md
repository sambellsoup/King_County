


# Predicting House Sales Price in King County


## Project Overview

With this data I had a few goals in mind. My short-term goal was to create a model in order to predict the price a house would sell for given a few variables. The dataset taken from Kaggle describes the price at which homes were sold in 2014-2015 as well as several features of the home: like whether it was on the waterfront, square footage, and location. 

<b> Key Questions: </b>
- Can we create a model to predict the price a house would sell for with a relative certainty?
- Which features of the home are most indicative of its value?

## Key Variables
### Target Variable: Price
### Feature Variables:
- id - Simple indexing of each entry in dataset
- date - The date the house was sold
- price - The monetary value the home was sold for in American dollars
- bedrooms - The number of bedrooms in the home
- bathrooms - The number of bathrooms in the home. A half bathroom means a toilet and a sink (no shower), and a quarter bathroom means only a sink.
- sqft_living - The amount of living space in the home.
- sqft_lot - The amount of land the home sits on.
- floors - How many levels the home has. 
- waterfront - Whether or not the home is directly near the water
- view - How good the view has been evaluated to be. This has been measured from 1-4. 1 indicates poor scenery, while 4 indicates very beautiful scenery.
- condition - The level of condition of the home. On a scale of 1-5, what condition is the home currently in? Does it need repairs? A 1 indicates poor condition, while a 5 indicates perfect condition. 
- grade - Measures the quality of materials used to construct the home. On a scale of 1-13. 1 indicates poor quality of materials while 13 indicates the best quality of materials. 
- sqft_above - Measures the amount of space in the home excluding the basement
- yr_built - Reflects the year the home was built
- yr_renovated - Tells the year the home was renovated
- zipcode - The zipcode where the home is.
- lat - Latitudinal coordinate of the home.
- long - Longitudinal coordinate of the home.
- sqft_living15 - Measures the sqft_living of the nearest 15 neighbors.
- sqft_lot15 - Measures the sqft_lot of the nearest 15 neighbors. 

More information can be found on the Kaggle Website <a
href=https://www.kaggle.com/harlfoxem/housesalesprediction>website</a>

## Data Collection and Analysis

Data from this database was examined and visualized. Not much cleaning was done; however, if I began to examine the years I would need to edit that column to only include the year. There were no null values. 

I did not remove any outliers from the data, nor did I transform or normalize the data in anyway. 

## Linear Regression Model Preparation and Creation

I evaluated how the features correlated with price as well as correlated with eachother. I picked 5 variables, which I believe had less of chance of colinearity. 

A training dataset for creating the linear regression model and a testing dataset was created by taking 80% of the data points for training and 20% for testing. 

The variables used in the linear regression model testing were sqft_living, grade, bathrooms, distance from epicenter, and waterfront. 










## Project Development
and my long-term goal is to include longitudinal data in order to predict a selling trend over time. With a longitudinal data set, I could also include tax appraisal in order to not only include the price of single-family homes, but also other buildings in the area. I would examine the borders of extremely valuable properties and considerably lower valued properties. I would want to identify the areas of highest value disparity within the closest proximity because these properties will most likely be bought by real estate developers in order to gain the maximum amount of profit. This typically happens in cities around the nation, and unfortunately this pattern of capitalism results in the displacement of many families who can no longer afford their rent. Since King County is developing at a rate faster than any other American city, the people who rent their homes are at a high risk of displacement. I would want to create a model that would pinpoint the areas most likely to be affected by gentrification over a ten-year span. Developers already work to pinpoint blocks that seem gentrifiable, which usually means buildings are in disrepair and are close to other gentrified areas. The rent gap is the disparity between how much a property is worth in its current state and how much it would be worth gentrified. The larger the gap in a neighborhood, the higher the chance it would gentrify. 

A rough equation to calculate the displacement risk may be:

 Number of nearby rich properties(mean tax appraisal of rich property) - Number of nearby poor properties(mean tax appraisal of cheap propert) 
 __________________________________________________________________
                         Distance
                         
The numerator of this expression should describe wealth disparity
 
 
 
 
 

## Objectives
You will be able to:
* Desequired deliverables
* Describe what constitutes a successful project
* Describe what the experience of the project review should be like

## Final Project Summary

You've made it all the way through the first module of this course - take a minute to celebrate your awesomeness! 

![awesome](https://raw.githubusercontent.com/learn-co-curriculum/dsc-v2-mod1-final-project/master/awesome.gif)

All that remains in Module 1 is to put our newfound data science skills to use with a final project! You should expect this project to take between 40 and 50 hours of solid, focused effort. If you're done way quicker, go back and dig in deeper or try some of the optional "level up" suggestions. If you're worried that you're going to get to 30 hrs and still not even have the data imported, reach out to an instructor in Slack ASAP to get some help!

## The Dataset

For this project, you'll be working with the King County House Sales dataset. We've modified the dataset to make it a bit more fun and challenging.  The dataset can be found in the file `"kc_house_data.csv"`, in this repo. 

The description of the column names can be found in the column_names.md file in this repository. As with most real world data sets, the column names are not perfectly described, so you'll have to do some research or use your best judgment if you have questions relating to what the data means.

You'll clean, explore, and model this dataset with a multivariate linear regression to predict the sale price of houses as accurately as possible. 

## The Deliverables

There will be four  deliverables for this project:

1. A well documented **Jupyter Notebook** containing any code you've written for this project and comments explaining it. This work will need to be pushed to your GitHub repository in order to submit your project.  
2. A short **Keynote/PowerPoint/Google Slides presentation** (delivered as a PDF export) giving a high-level overview of your methodology and recommendations for non-technical stakeholders.	2. A short **Keynote/PowerPoint/Google Slides presentation** (delivered as a PDF export) giving a high-level overview of your methodology and recommendations for non-technical stakeholders. Make sure to also add and commit this pdf of your non-technical presentation to your repository with a file name of presentation.pdf.
3. **A blog post** (800-1500 words) about one element of the project - it could be the EDA, the feature selection, the choice of visualizations or anything else technical relating to the project. It should be targeted at your peers - aspiring data scientists.	3. A **blog post** (800-1500 words) about one element of the project - it could be the EDA, the feature selection, the choice of visualizations or anything else technical relating to the project. It should be targeted at your peers - aspiring data scientists.
4. A **Video Walkthrough** of your non-technical presentation. Some common video recording tools used are Zoom, Quicktime, and Nimbus. After you record your presentation, publish it on a service like YouTube or Google Drive, you will need a link to the video to submit your project.

## The Process

### 1. Getting Started

Please start by reviewing this document. If you have any questions, please ask them in slack ASAP so (a) we can answer the questions and (b) so we can update this repository to make it clearer.

 Be sure to let the instructor team know when you’ve started working on a project, either by reaching out over Slack or, if you are in a full-time or part-time cohort, by connecting with your Cohort Lead in your weekly 1:1. If you’re not sure who to reach out to, post in the #online-ds-sp-000 channel in Slack.

Once you're done with the first 12 sections, please start on the project. Do that by forking this repository, cloning it locally, and working in the student.ipynb file. Make sure to also add and commit a pdf of your presentation to the repository with a file name of `presentation.pdf`.

### 2. The Project Review

> **When you start on the project, please also reach out to an instructor immediately to schedule your project review** (if you're not sure who to schedule with, please ask in slack!)

#### What to expect from the Project Review

Project reviews are focused on preparing you for technical interviews. Treat project reviews as if they were technical interviews, in both attitude and technical presentation *(sometimes technical interviews will feel arbitrary or unfair - if you want to get the job, commenting on that is seldom a good choice)*.

The project review is comprised of a 45 minute 1:1 session with one of the instructors. During your project review, be prepared to:

#### 1. Deliver your PDF presentation to a non-technical stakeholder. 
In this phase of the review (~10 mins) your instructor will play the part of a non-technical stakeholder that you are presenting your findings to. The presentation should not exceed 5 minutes, giving the "stakeholder" 5 minutes to ask questions.

In the first half of the presentation (2-3 mins), you should summarize your methodology in a way that will be comprehensible to someone with no background in data science and that will increase their confidence in you and your findings. In the second half (the remaining 2-3 mins) you should summarize your findings and be ready to answer a couple of non-technical questions from the audience. The questions might relate to technical topics (sampling bias, confidence, etc) but will be asked in a non-technical way and need to be answered in a way that does not assume a background in statistics or machine learning. You can assume a smart, business stakeholder, with a non-quantitative college degree.

#### 2. Go through the Jupyter Notebook, answering questions about how you made certain decisions. Be ready to explain things like:
    * "how did you pick the question(s) that you did?"
    * "why are these questions important from a business perspective?"
    * "how did you decide on the data cleaning options you performed?"
    * "why did you choose a given method or library?"
    * "why did you select those visualizations and what did you learn from each of them?"
    * "why did you pick those features as predictors?"
    * "how would you interpret the results?"
    * "how confident are you in the predictive quality of the results?"
    * "what are some of the things that could cause the results to be wrong?"

Think of the first phase of the review (~30 mins) as a technical boss reviewing your work and asking questions about it before green-lighting you to present to the business team. You should practice using the appropriate technical vocabulary to explain yourself. Don't be surprised if the instructor jumps around or sometimes cuts you off - there is a lot of ground to cover, so that may happen.

If any requirements are missing or if significant gaps in understanding are uncovered, be prepared to do one or all of the following:
* Perform additional data cleanup, visualization, feature selection, modeling and/or model validation
* Submit an improved version
* Meet again for another Project Review

What won't happen:
* You won't be yelled at, belittled, or scolded
* You won't be put on the spot without support
* There's nothing you can do to instantly fail or blow it

**Please note: We need to receive the URL of your repository at least 24 hours before and please have the project finished at least 3 hours before your review so we can look at your materials in advance.** 


## Requirements

This section outlines the rubric we'll use to evaluate your project.

### 1. Technical Report Must-Haves

For this project, your Jupyter Notebook should meet the following specifications:

#### Organization/Code Cleanliness

* The notebook should be well organized, easy to follow,  and code should be commented where appropriate.  
    * Level Up: The notebook contains well-formatted, professional looking markdown cells explaining any substantial code.  All functions have docstrings that act as professional-quality documentation
* The notebook is written for technical audiences with a way to both understand your approach and reproduce your results. The target audience for this deliverable is other data scientists looking to validate your findings. 

#### Visualizations & EDA

* Your project contains at least 4 meaningful data visualizations, with corresponding interpretations. All visualizations are well labeled with axes labels, a title, and a legend (when appropriate)  
* You pose at least 3 meaningful questions and answer them through EDA.  These questions should be well labeled and easy to identify inside the notebook. 
    * **Level Up**: Each question is clearly answered with a visualization that makes the answer easy to understand.   
* Your notebook should contain 1 - 2 paragraphs briefly explaining your approach to this project.
    
#### Model Quality/Approach

* Your model should not include any predictors with p-values greater than .05.  
* Your notebook shows an iterative approach to modeling, and details the parameters and results of the model at each iteration.  
    * **Level Up**: Whenever necessary, you briefly explain the changes made from one iteration to the next, and why you made these choices.  
* You provide at least 1 paragraph explaining your final model.   
* You pick at least 3 coefficients from your final model and explain their impact on the price of a house in this dataset.   


### 2. Non-Technical Presentation Must-Haves

The second deliverable should be a Keynote, PowerPoint or Google Slides presentation delivered as a pdf file in your fork of this repository with the file name of `presentation.pdf` detailing the results of your project.  Your target audience is non-technical people interested in using your findings to maximize their profit when selling their home. 

Your presentation should:

* Contain between 5 - 10 professional-quality slides.  
    * **Level Up**: The slides should use visualizations whenever possible, and avoid walls of text. 
* Take no more than 5 minutes to present.   
* Avoid technical jargon and explain the results in a clear, actionable way for non-technical audiences.   

**_Based on the results of your models, your presentation should discuss at least two concrete features that highly influence housing prices._**

### 3. Blog Post

Please also write a blog post about one element of the project - it could be the EDA, the feature selection, the choice of visualizations or anything else technical relating to the project. It should be between 800-1500 words and should be targeted at your peers - aspiring data scientists.

## Submitting your Project

 You’re almost done! In order to submit your project for review, include the following links to your work in the corresponding fields on the right-hand side of Learn.

 1. **GitHub Repo:** Now that you’ve completed your project in Jupyter Notebooks, push your work to GitHub and paste that link to the right. (If you need help doing so, review the resources [here](https://docs.google.com/spreadsheets/d/1CNGDhjcQZDRx2sWByd2v-mgUOjy13Cd_hQYVXPuzEDE/edit#gid=0).)
_Reminder: Make sure to also add and commit a pdf of your non-technical presentation to the repository with a file name of presentation.pdf._
2. **Blog Post:** Include a link to your blog post.
3. **Record Walkthrough:** Include a link to your video walkthrough.

 Hit "I'm done" to wrap it up. You will receive an email in order to schedule your review with your instructor.


## Summary

The end of module projects and project reviews are a critical part of the program. They give you a chance to both bring together all the skills you've learned into realistic projects and to practice key "business judgement" and communication skills that you otherwise might not get as much practice with.

The projects are serious and important. They are not graded, but they can be passed and they can be failed. Take the project seriously, put the time in, ask for help from your peers or instructors early and often if you need it, and treat the review as a job interview and you'll do great. We're rooting for you to succeed and we're only going to ask you to take a review again if we believe that you need to. We'll also provide open and honest feedback so you can improve as quickly and efficiently as possible.

Finally, this is your first project. We don't expect you to remember all of the terms or to get all of the answers right. If in doubt, be honest. If you don't know something, say so. If you can't remember it, just say so. It's very unusual for someone to complete a project review without being asked a question they're unsure of, we know you might be nervous which may affect your performance. Just be as honest, precise and focused as you can be, and you'll do great!

