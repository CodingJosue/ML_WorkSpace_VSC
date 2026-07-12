# ML Questions
## 1. What are we trying to predict?
I am predicting if a person has heart disease yes or no?

## 2. Can you ML it?
Yes!
The alternative to ML: Writing complex if-then rules by hand ("if cholesterol > X and age > Y and chest pain type = Z, then..."). This gets messy fast.

What ML does instead: Learns the patterns from examples, so you don't have to hand-code the rules.

## 3.What type of problem is this ?
This is a classic classification problem because our main goal is to put into a bucket whether a person has heart disease or not. It is specifically called binary classification because we have two choices: has heart disease or doesn't have heart disease. Why is this not a linear regression problem? Unlike a classification problem, a linear regression problem requires that you're trying to predict a value on a continuous scale. Meaning that, for example, the exact price of a house is not putting things in a bucket because each house is going to vary in price. You cannot say, "Oh, this house, every house that falls into that category," because each value changes.  


## 4.Who is this model for ?

So, based on who this model is for, our accuracy is going to vary, okay? 
1. If it is for a doctor, then we want high accuracy, meaning that maybe in the 99 to 100
2. If it is for researchers, maybe we don't need to be that accurate because the researchers just want to guide their research. Maybe it is at 70-80% accuracy. 
3. If it is an at-home test, maybe we don't even need to be that accurate. It can be between, let's say, 60% and 70% to just give an idea to a person based on certain home results. 




## 5. What mistakes can we tolerate?
Scenario A: The model says "no heart disease" but the patient actually has it. The patient goes home, has a heart attack a week later.

Scenario B: The model says "has heart disease" but the patient is actually healthy. The patient gets unnecessary tests, panic, and medical bills.

So, Scenario A is a false negative and scenario B is a false positive. The worst scenario is obviously A because the person does have the disease and the person dies because the person was not diagnosed.

What metric you optimize for (we'll talk about this later — but you'll want to favor recall over precision)

How you set your decision threshold (maybe you make the model more sensitive, even if it means more false alarms)

How you present results (you'll emphasize "we caught X% of actual cases" rather than just "we were right Y% of the time")