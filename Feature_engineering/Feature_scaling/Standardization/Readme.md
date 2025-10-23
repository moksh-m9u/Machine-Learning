# Feature Scaling 
- it is a technique to standardise the independent features present in data in a fixed range            

- it is generally the last step in feature engineering          

---

## Importance of feature scaling

- it is important for all the features to be in similar scale as otherwise algorthim such as kNN where euclidian distance has to be caluclated wont work accurately         

![alt text](<Screenshot 2025-10-22 at 5.08.59 PM.png>)

here lets say if we have two features       
1. salary (x)
2. age (y)

now for any algortihm working on these features the scale of these features are diff ie (0-80 for age and 10k - 200k for salary).       

here in this case the y term wont be able to influence and show its impact on the algorithm 

thus it is imp for both the feature to be in the same scale.   

---
 ## Types of features scaling
 1. Standardiasation - also called as Z-score normalisation
 2. Normalisation
    - Min Max scaler
    - Robust scaler

---

## Standardisation

Standardisation transforms data to have mean = 0 and standard deviation = 1 using the formula:   

**Z = (X - μ)/σ**

Where:
- Z = standardized value
- X = original value  
- μ = mean of the feature
- σ = standard deviation of the feature

### Dummy Dataset Example

| Person | Age (X) | Salary (Y) | Age Standardized (X') | Salary Standardized (Y') |
|--------|---------|------------|----------------------|-------------------------|
| 1      | 25      | 45000      | -1.41                | -1.34                   |
| 2      | 35      | 65000      | -0.71                | -0.67                   |
| 3      | 45      | 85000      | 0.00                 | 0.00                    |
| 4      | 55      | 105000     | 0.71                 | 0.67                    |
| 5      | 65      | 125000     | 1.41                 | 1.34                    |

**Calculations:**
- Age: Mean (μ) = 45, Standard Deviation (σ) = 14.14
- Salary: Mean (μ) = 85000, Standard Deviation (σ) = 29814.24

**Example calculation for Person 1:**
- Age Standardized: (25 - 45) / 14.14 = -1.41
- Salary Standardized: (45000 - 85000) / 29814.24 = -1.34

After standardisation, both features now have similar scales ranging approximately from -1.5 to +1.5.

---

## Geometric intution

- Mean Centring - Basically we are trying to shift the mean to origin by standardiasation

- Scaling by the factor of std deviation (ye abhi clear nahi hua muje)

---
## Impact of outliers

- 