# One Hot Encoding

## Whats covered in this folder

- (One hot encoding -> Dummy variable Trap -> OHE using most frequenet variable)

## Brief overview
- Nominal data :categorical data with no hierearchy or order (eg of heirarchial data is grades: poor, good , average)
- example of nominal data : Colours , country names , animal name
- here no hierarchy exists

## About One hot encoding and why do we even need it?

- in nominal dataset we can not use ordinal encoding as there is no order of hieracrchy
- the main reason for not using ordinal encoding is that it might mislead the algorithm that few values have higher hierarchial order than others
- for example: we can not assign binary encoding to genders like males : 0 and females:1
- this would miselad our algo that females are at higher hierachy than males while both are equal (nominal)
- a similar ex for colours can be taken 

**disclaimer - the above example was just in relevance of nominal dataset and nothing to do with my opinions on gender war**

## Then what exactly is one hot encoding

- here we assign a matrix or vector where values are assigned in such a manner as given in the ex below

| ID | Color_Red | Color_Blue | Color_Green | Size_Small | Size_Medium | Size_Large |
|----|------------|-------------|--------------|-------------|--------------|-------------|
| 1  | 1 | 0 | 0 | 1 | 0 | 0 |
| 2  | 0 | 1 | 0 | 0 | 1 | 0 |
| 3  | 0 | 0 | 1 | 0 | 0 | 1 |
| 4  | 1 | 0 | 0 | 0 | 0 | 1 |
| 5  | 0 | 1 | 0 | 1 | 0 | 0 |

---
##  Color Encoding Vectors

| Color | One-Hot Vector (Red, Blue, Green) |
|--------|------------------------------------|
| Red    | [1, 0, 0] |
| Blue   | [0, 1, 0] |
| Green  | [0, 0, 1] |


---

## Row wise Color Vectors from Datasat

| ID | Color_Red | Color_Blue | Color_Green | Vector Representation |
|----|------------|-------------|--------------|------------------------|
| 1  | 1 | 0 | 0 | [1, 0, 0] |
| 2  | 0 | 1 | 0 | [0, 1, 0] |
| 3  | 0 | 0 | 1 | [0, 0, 1] |
| 4  | 1 | 0 | 0 | [1, 0, 0] |
| 5  | 0 | 1 | 0 | [0, 1, 0] |

---
## Key Take awayss:
- Each **color** is represented as a **3-dimensional binary vector**.  
- Only one element in the vector is **1**, marking the active category.  
- This prevents the model from assigning any **ordinal meaning** to colors.  
- Example: Red ≠ twice Blue or half Green : they’re all **equally distant** in vector space.


---
---

# Dummy variable trap

- Whenever we apply One hot encoding we only apply it for n-1 columns
- so lets say if we have to represent 4 colours we will only have encoding matrix for three of them 
lets say we have 4 colours - Red , Blue , Green and Yellow

| Color | One-Hot Vector (Red, Blue, Green) |
|--------|------------------------------------|
| Red    | [1, 0, 0] |
| Blue   | [0, 1, 0] |
| Green  | [0, 0, 1] |

Now its very obvious if all elements of the vector are zero so the colour is yellow

## But the ques here is why do we did so?

- to Reduce dimmensionality which is like a side reason
- the main reason is to prevent Multicolinerairty 

### But what is multicolinearity

- when Input columns in our data have some mathematical relationship among themselves
- Input columns must be independenet from each other
- our prediction column or target value is often the dependent column which is dependent on these input columns 
- but these input columns (x) having dependency on each other is not ideal for a ml model to make predictions
- IN short input colmns must be independent of each other

- Linear model hates multicolinearity
    - Linear regression and logistic regressions are linear models which do not works good with multicolinearity

### Can we see a relationship in our data without the dummy variable trap method

yes the problem if we dont remove one column is that sum of matrix for all the columns or input variable becomes one

- so here multicolinearity exists as shown in table below

## Without Removing Any Column (Dummy Variable Trap Present)

| Color  | Red | Blue | Green | Yellow | Sum |
|--------|-----|------|--------|---------|-----|
| Red    | 1 | 0 | 0 | 0 | 1 |
| Blue   | 0 | 1 | 0 | 0 | 1 |
| Green  | 0 | 0 | 1 | 0 | 1 |
| Yellow | 0 | 0 | 0 | 1 | 1 |

### Problem:
- The **sum of all dummy columns = 1** for every row.  
- This means one column can be **predicted from the others**:
- (multicolinearity)

## After Removing One Column (Dummy Variable Trap Avoided)

We drop one column (e.g., **Yellow**) because it can be inferred when all others are 0.

| Color  | Red | Blue | Green |
|--------|-----|------|--------|
| Red    | 1 | 0 | 0 |
| Blue   | 0 | 1 | 0 |
| Green  | 0 | 0 | 1 |
| Yellow | 0 | 0 | 0 |

###  Solution:
- No column is a **linear combination** of the others.  
- Now the dataset has **independent variables**.  
- Linear models like **Linear Regression** and **Logistic Regression** work properly.

---

### **When performing **One-Hot Encoding**, always use **n−1 dummy columns** to avoid multicollinearity and ensure your model learns correctly.**

---
# One hot Encoding using most frequent variables






