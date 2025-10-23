# Encoding Categorical Data

### Data has two types
1. Numerical - number wala
2. Categoriccal - strings 

#### under Categorical we have further two types
1. Nominal
    - no inhertance order
    - Categories dont have any order or relation
    - example ke lie name of states maanlo
2. ordinal
    - high school me marks ki categories lelo ex ke lie
    - distinction , pass , fail
    - so here we have order of categorical data

---

#### Algorithms need numerical data to predict so here we are 
- ML models cant handle strings or categorical data directtly so we have to encode them
- our main goal while encoding is to convert the categorical data into numerical one using encoding

---
## Types of Encoding
1. Ordinal ecnoding- ordinal data 
2. One Hot Encoding- Nominal data

---
## Label Encoding vs Ordinal encoding

1. Label encoding : used for both ordinal and nominal data
    - here we assign integers to categorical data 
    - so each category has a unique integer
    - example - red - 0 , blue- 1 , green 2
    -algo : Tree based models or categorical target variable(y).  
     
    ***IT SHOULD ONLY BE USED FOR TARGET VALUES I.E. Y AND NOT INPUT VARIIABLES***

2. One Hot encoding : generally used for nominal data
    - it creates a binary column or matrix for each category
    - example  , red [1,0,0] ; blue[0,1,0] ; green[0,0,1]
    - nominal data

3. Ordinal Encoding
    - as the name says oridnal data ke sath use hoga
    - Each category is replaced with an integer reflecting its rank.  
    - Example: `Low → 1`, `Medium → 2`, `High → 3`  
    - Preserves **order relationships**, making it suitable for **ordinal data**.  
    - Not suitable for nominal data, as numeric order could mislead the model.
