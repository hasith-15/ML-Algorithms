
 #LINEAR Regression.

#Senario: A company is trying to understand the relationship between the number of years of experience and its employe’s salary. By analysing this relationship,the company hopes to be able to predict the salary of new hires based on their years of experience.


#Process:
## Data Table

| Mean of (X) | Mean of (Y) | Dev of (X) (xi - x̄) | Dev of (Y) (yi - ȳ) | Product of Deviation ((xi - x̄)(yi - ȳ)) | Sum of Product of Deviation (Σ (xi - x̄)(yi - ȳ)) | Square of Dev (X) ((xi - x̄)²) | Square of Dev (Y) ((yi - ȳ)²) |
|-------------|-------------|---------------------|---------------------|-----------------------------------------|--------------------------------------------------|-------------------------------|-------------------------------|
| 2.32        | 48,675      | -1.22               | -9,332              | 11,885                                  | 56,063                                           | 1.4884                        | 87,086,724                    |
| 2.32        | 48,675      | -1.02               | -2,470              | 2,519                                   |                                                  | 1.0404                        | 6,100,900                     |
| 2.32        | 48,675      | -0.82               | -10,944             | 8,974                                   |                                                  | 0.6724                        | 119,771,936                   |
| 2.32        | 48,675      | -0.32               | -5,150              | 1,648                                   |                                                  | 0.1024                        | 26,522,500                    |
| 2.32        | 48,675      | -0.12               | -8,784              | 1,054                                   |                                                  | 0.0144                        | 77,158,656                    |
| 2.32        | 48,675      | 0.58                | 7,967               | 4,620                                   |                                                  | 0.3364                        | 63,473,089                    |
| 2.32        | 48,675      | 0.68                | 11,475              | 7,803                                   |                                                  | 0.4624                        | 131,675,625                   |
| 2.32        | 48,675      | 0.88                | 11,475              | 10,098                                  |                                                  | 0.7744                        | 131,675,625                   |
| 2.32        | 48,675      | 1.38                | 5,770               | 7,962                                   |                                                  | 1.9044                        | 33,292,900                    |
| **Sum:** |             | **0.00** | **0** | **56,063** | **56,063** | **6.7916** | **676,757,955** |

# Calculation Steps

# 1. Calculate the Slope (M)

The slope (M) represents the change in Y for every one-unit change in X.
The formula for the slope is:
$M = \frac{\text{Sum of Product of Deviation}}{\text{Sum of Square of Dev(X)}}$

Given:
* Sum of Product of Deviation = 56,063
* Sum of Square of Dev(X) = 6.7916

Calculation:
$M = \frac{56,063}{6.7916}$
$M = 8,254.75$

# 2. Calculate the Y-intercept (b)

The Y-intercept (b) is the value of Y when X is 0.
The formula for the Y-intercept is:
$b = \text{mean(Y)} - (M \times \text{mean(X)})$

Given:
* Mean of (Y) = 48,675
* Mean of (X) = 2.32
* Slope (M) = 8,254.75

Calculation:
$b = 48,675 - (8,254.75 \times 2.32)$
$b = 48,675 - 19,151$
$b = 29,524$

# 3. Linear Regression Equation

The simple linear regression equation is given by:
$Y = M \times X + b$

Substituting the calculated values of M and b:
$Y = 8,254.75 \times X + 29,524$

# 4. Predicting Salary for a Given Experience (Example)

# # # Let's predict the salary for an experience of 5.0 years.

Given:
* Experience (X) = 5.0 years

Calculation:
$\text{Salary} = 8,254.75 \times 5.0 + 29,524$
$\text{Salary} = 41,273.75 + 29,524$
$\text{Salary} = 70,797.75$

Therefore, the predicted salary for someone with 5.0 years of experience is $70,797.75.


# Complete Linkage Clustering

## Complete Clustering# Hierarchical Clustering Analysis: Patient Health Profiles

This repository demonstrates a step-by-step complete linkage hierarchical clustering analysis applied to a dataset of patient health profiles. The goal is to identify distinct patient segments based on Blood Pressure Index (BPI) and Resting Heart Rate (HR).

## Table of Contents
- [Scenario](#scenario)
- [Data](#data)
- [Question](#question)
- [Instructions](#instructions)
- [Detailed Answer](#detailed-answer)
    - [1. Initial Pairwise Distance Matrix (Euclidean Distance)](#1-initial-pairwise-distance-matrix-euclidean-distance)
    - [2. Clustering Steps (Complete Linkage)](#2-clustering-steps-complete-linkage)
    - [3. Dendrogram Representation](#3-dendrogram-representation)

---

## Scenario

A medical researcher is studying patient health profiles based on two critical physiological indicators: 'Blood Pressure Index' (BPI) and 'Resting Heart Rate' (HR, in beats per minute). The researcher has collected data from 5 patients and wants to group them into clusters to identify potential patient segments that might require similar medical attention or lifestyle advice.

## Data

The following are the BPI and HR measurements for 5 patients:

| Patient | Blood Pressure Index (X) | Heart Rate (Y) |
|---------|--------------------------|----------------|
| P1      | 120                      | 70             |
| P2      | 122                      | 72             |
| P3      | 145                      | 60             |
| P4      | 148                      | 62             |
| P5      | 118                      | 90             |

## Question

Using the **Euclidean distance** as the dissimilarity measure, perform a complete linkage hierarchical clustering on these patient data points.

## Instructions

1.  Calculate the initial pairwise distance matrix between all patients.
2.  Show each step of the clustering process, clearly indicating which clusters are merged and the dissimilarity value (height) at which they merge.
3.  For each merge step, update the distance matrix according to the complete linkage rule.
4.  Finally, draw the dendrogram that visually represents the complete linkage clustering process.

---

## Detailed Answer: Patient Health Profiles Clustering

### 1. Initial Pairwise Distance Matrix (Euclidean Distance)

The Euclidean distance between two points $(x_1, y_1)$ and $(x_2, y_2)$ is given by $\sqrt{(x_2-x_1)^2 + (y_2-y_1)^2}$.

Let's calculate the distances:

* $d(P1, P2) = \sqrt{(122-120)^2 + (72-70)^2} = \sqrt{2^2 + 2^2} = \sqrt{4+4} = \sqrt{8} \approx 2.83$
* $d(P1, P3) = \sqrt{(145-120)^2 + (60-70)^2} = \sqrt{25^2 + (-10)^2} = \sqrt{625+100} = \sqrt{725} \approx 26.93$
* $d(P1, P4) = \sqrt{(148-120)^2 + (62-70)^2} = \sqrt{28^2 + (-8)^2} = \sqrt{784+64} = \sqrt{848} \approx 29.12$
* $d(P1, P5) = \sqrt{(118-120)^2 + (90-70)^2} = \sqrt{(-2)^2 + 20^2} = \sqrt{4+400} = \sqrt{404} \approx 20.10$
* $d(P2, P3) = \sqrt{(145-122)^2 + (60-72)^2} = \sqrt{23^2 + (-12)^2} = \sqrt{529+144} = \sqrt{673} \approx 25.94$
* $d(P2, P4) = \sqrt{(148-122)^2 + (62-72)^2} = \sqrt{26^2 + (-10)^2} = \sqrt{676+100} = \sqrt{776} \approx 27.86$
* $d(P2, P5) = \sqrt{(118-122)^2 + (90-72)^2} = \sqrt{(-4)^2 + 18^2} = \sqrt{16+324} = \sqrt{340} \approx 18.44$
* $d(P3, P4) = \sqrt{(148-145)^2 + (62-60)^2} = \sqrt{3^2 + 2^2} = \sqrt{9+4} = \sqrt{13} \approx 3.61$
* $d(P3, P5) = \sqrt{(118-145)^2 + (90-60)^2} = \sqrt{(-27)^2 + 30^2} = \sqrt{729+900} = \sqrt{1629} \approx 40.36$
* $d(P4, P5) = \sqrt{(118-148)^2 + (90-62)^2} = \sqrt{(-30)^2 + 28^2} = \sqrt{900+784} = \sqrt{1684} \approx 41.04$

Initial Distance Matrix:

|      | P1     | P2     | P3     | P4     | P5     |
|------|--------|--------|--------|--------|--------|
| **P1** | 0.00   | 2.83   | 26.93  | 29.12  | 20.10  |
| **P2** | 2.83   | 0.00   | 25.94  | 27.86  | 18.44  |
| **P3** | 26.93  | 25.94  | 0.00   | 3.61   | 40.36  |
| **P4** | 29.12  | 27.86  | 3.61   | 0.00   | 41.04  |
| **P5** | 20.10  | 18.44  | 40.36  | 41.04  | 0.00   |

### 2. Clustering Steps (Complete Linkage)

Complete linkage clustering merges the two clusters whose *maximum* distance between any two points (one from each cluster) is the smallest.

**Step 1: Merge P1 and P2**

The smallest distance in the initial matrix is $d(P1, P2) = 2.83$.

New cluster: `{P1, P2}` at height 2.83.

Now, we calculate distances from `{P1, P2}` to other points/clusters using complete linkage:
* $d(\{P1, P2\}, P3) = \max(d(P1, P3), d(P2, P3)) = \max(26.93, 25.94) = 26.93$
* $d(\{P1, P2\}, P4) = \max(d(P1, P4), d(P2, P4)) = \max(29.12, 27.86) = 29.12$
* $d(\{P1, P2\}, P5) = \max(d(P1, P5), d(P2, P5)) = \max(20.10, 18.44) = 20.10$

Updated Distance Matrix:

|           | {P1,P2} | P3     | P4     | P5     |
|-----------|---------|--------|--------|--------|
| **{P1,P2}** | 0.00    | 26.93  | 29.12  | 20.10  |
| **P3** | 26.93   | 0.00   | 3.61   | 40.36  |
| **P4** | 29.12   | 3.61   | 0.00   | 41.04  |
| **P5** | 20.10   | 40.36  | 41.04  | 0.00   |

**Step 2: Merge P3 and P4**

The minimum distance in the updated matrix is $d(P3, P4) = 3.61$.

New cluster: `{P3, P4}` at height 3.61.

Now, calculate distances from `{P3, P4}` to other points/clusters:
* $d(\{P3, P4\}, \{P1, P2\}) = \max(d(P3, \{P1, P2\}), d(P4, \{P1, P2\}))$
    $= \max(26.93, 29.12) = 29.12$
* $d(\{P3, P4\}, P5) = \max(d(P3, P5), d(P4, P5)) = \max(40.36, 41.04) = 41.04$

Updated Distance Matrix:

|           | {P1,P2} | {P3,P4} | P5     |
|-----------|---------|---------|--------|
| **{P1,P2}** | 0.00    | 29.12   | 20.10  |
| **{P3,P4}** | 29.12   | 0.00    | 41.04  |
| **P5** | 20.10   | 41.04   | 0.00   |

**Step 3: Merge P5 and {P1,P2}**

The minimum distance in the updated matrix is $d(\{P1, P2\}, P5) = 20.10$.

New cluster: `{{P1, P2}, P5}` at height 20.10.

Now, calculate distance from `{{P1, P2}, P5}` to `{P3, P4}`:
* $d(\{\{P1, P2\}, P5\}, \{P3, P4\}) = \max(d(\{P1, P2\}, \{P3, P4\}), d(P5, \{P3, P4\}))$
    $= \max(29.12, 41.04) = 41.04$

Updated Distance Matrix:

|                 | {{P1,P2},P5} | {P3,P4} |
|-----------------|--------------|---------|
| **{{P1,P2},P5}** | 0.00         | 41.04   |
| **{P3,P4}** | 41.04        | 0.00    |

**Step 4: Merge {{P1,P2},P5} and {P3,P4}**

The final merge is between these two large clusters at a distance of 41.04.

Final cluster: `{{{P1, P2}, P5}, {P3, P4}}` at height 41.04.

### 3. Dendrogram Representation

Here's the dendrogram representing the complete linkage clustering process:

Height
41.04 +---------------------------------+
|                                 |
|                                 |
|                     +-----------+-----------+
|                     |                       |
|                     |                       |
20.10 +---------------------+                       |
|                     |                       |
|                     |                       |
|           +----+----+                       |
|           |         |                       |
|           |         |                       |
3.61  +-----+-----+         |                       |
|     |     |         |                       |
|     |     |         |                       |
2.83  +-----+-----+----+---------+------------------+
|     |     |    |         |                  |
|     |     |    |         |                  |
0     +-----+-----+----+---------+------------------+
P1    P2    P5    P3    P4


**Explanation of the Dendrogram:**

* **Leaves:** At the bottom, each patient (P1, P2, P3, P4, P5) starts as a single cluster.
* **Vertical Lines (Height):** The height of the merge point on the vertical axis represents the dissimilarity (Euclidean distance) at which the clusters were joined.
* **Horizontal Lines:** These connect the branches that are being merged.
* **First Merges:**
    * P1 and P2 merge at a height of approximately 2.83, forming a cluster `{P1, P2}\}$. This indicates they are quite similar in their health profiles.
    * P3 and P4 merge at a height of approximately 3.61, forming a cluster `{P3, P4}\}$. They are also relatively close to each other.
* **Subsequent Merges:**
    * Patient P5 then merges with the `{P1, P2}` cluster at a height of 20.10, forming the cluster `{{P1, P2}, P5}\}$. This means that P5's profile is more similar to the "furthest" of P1 or P2 (due to complete linkage) than to any other point outside this group at this stage.
    * Finally, the large cluster `{{P1, P2}, P5}` merges with the `{P3, P4}` cluster at a height of 41.04. This is the largest distance, indicating these two major patient groups are quite distinct from each other.

The dendrogram visually confirms that P1, P2, and P5 form one broad group (patients with lower BPI but varying HR, where P5 has a significantly higher HR), while P3 and P4 form another distinct group (patients with higher BPI and lower HR). The final merge shows the overall dissimilarity between these two major patient segments.

# Single-Linkage Clustering for Athletic Shoe Performance

This document outlines the process of grouping similar athletic shoes based on their **Agility Score** and **Durability Score** using **Single-Linkage Clustering**.  
The analysis is intended to help a data analyst at a Sports Equipment Company design more targeted marketing strategies.

---

# 📊 Data

The dataset includes Agility Score (x) and Durability Score (y) for six different athletic shoes:

| Shoe | Agility Score (x) | Durability Score (y) |
|------|--------------------|-----------------------|
| A    | 2                  | 8                     |
| B    | 3                  | 7                     |
| C    | 6                  | 4                     |
| D    | 7                  | 5                     |
| E    | 9                  | 2                     |
| F    | 8                  | 3                     |

---

#Step 1: Calculate Euclidean Distances

The Euclidean distance formula:

distance = √[(x2 - x1)² + (y2 - y1)²]

yaml
Copy
Edit

Calculated distances:

- d(A, B) ≈ 1.41  
- d(A, C) ≈ 5.65  
- d(A, D) ≈ 5.83  
- d(A, E) ≈ 9.21  
- d(A, F) ≈ 7.81  
- d(B, C) ≈ 4.24  
- d(B, D) ≈ 4.47  
- d(B, E) ≈ 7.81  
- d(B, F) ≈ 6.40  
- d(C, D) ≈ 1.41  
- d(C, E) ≈ 3.60  
- d(C, F) ≈ 2.23  
- d(D, E) ≈ 3.60  
- d(D, F) ≈ 2.23  
- d(E, F) ≈ 1.41

---

# Step 2: Distance Matrix

|     | A    | B    | C    | D    | E    | F    |
|-----|------|------|------|------|------|------|
| A   | 0    | 1.41 | 5.65 | 5.83 | 9.21 | 7.81 |
| B   | 1.41 | 0    | 4.24 | 4.47 | 7.81 | 6.40 |
| C   | 5.65 | 4.24 | 0    | 1.41 | 3.60 | 2.23 |
| D   | 5.83 | 4.47 | 1.41 | 0    | 3.60 | 2.23 |
| E   | 9.21 | 7.81 | 3.60 | 3.60 | 0    | 1.41 |
| F   | 7.81 | 6.40 | 2.23 | 2.23 | 1.41 | 0    |

---

# 🔗 Step 3: Single-Linkage Clustering

### Iteration 1:

Minimum distances:
- d(A, B) = 1.41  
- d(C, D) = 1.41  
- d(E, F) = 1.41  

Form clusters:
- (A, B)  
- (C, D)  
- (E, F)  

New distance matrix:

|       | (A,B) | (C,D) | (E,F) |
|-------|-------|-------|-------|
| (A,B) | 0     | 4.24  | 6.40  |
| (C,D) | 4.24  | 0     | 2.23  |
| (E,F) | 6.40  | 2.23  | 0     |

---

# Iteration 2:

Minimum distance:
- d((C,D), (E,F)) = 2.23

Form new cluster: **(C,D,E,F)**

New distance matrix:

|           | (A,B) | (C,D,E,F) |
|-----------|-------|-----------|
| (A,B)     | 0     | 4.24      |
| (C,D,E,F) | 4.24  | 0         |

---

### Iteration 3:

Minimum distance:
- d((A,B), (C,D,E,F)) = 4.24

Final cluster: **(A,B,C,D,E,F)**

---

## Dendrogram Summary

Distance ~1.41: (A,B), (C,D), (E,F)
Distance ~2.23: (C,D,E,F)
Distance ~4.24: (A,B,C,D,E,F)

yaml
Copy
Edit

---

# Conclusion

This Single-Linkage Clustering analysis has grouped the athletic shoes based on performance similarity. These clusters can guide targeted marketing campaigns, such as bundling similar-performing shoes or creating product segments.



 

