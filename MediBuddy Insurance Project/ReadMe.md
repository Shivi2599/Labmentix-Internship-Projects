# MediBuddy Insurance Project

## Table of Contents
- [Overview](#overview)
- [Purpose Statement](#purpose-statement)
- [Dataset-Overview](#dataset-overview)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Key Business Question and Insights](#key-business-question-and-insights)
- [Conclusion](#conclusion)
  
## Overview

MediBuddy is a digital healthcare platform for an inpatient hospitalization, outpatient services, and corporate wellness benefits.
MediBuddy is the award-winning technology platform from Medi Assist that transforms the health insurance industry at the very core. MediBuddy, with its diverse offerings for various stakeholders of the health benefits industry, makes the process of discovering, accessing, utilizing, and monitoring health benefits seamless, real-time, and virtually paperless.

## Purpose Statement

Identify if the key factors like **gender, BMI, age, smoking status, geographic  location, and number of dependents influences** insurance claims and policy costs.

## Dataset Overview:

The assignment provided two datasets:

- One containing age and BMI, collected before policy coverage.

- Another with personal details, including number of children, smoking status, and geographic location.

## Exploratory Data Analysis

- **Gender Distribution:** 676 males, 662 females.

- **Age Range:** 18 to 64 years, with an average of ~39 years.

- **BMI Range:** 15.96 to 53.13, with an average of ~30.66.

- **Insurance Charges:** Highly variable, ranging from ₹1,121.87 to ₹63,770.42.

- **Children (Dependents):** 0 to 5 dependents, with most having 0-2 children.

- **Smokers vs. Non-Smokers:** 1,064 are non-smokers, 274 are smokers.

- **Regional Distribution:** Southeast has the highest count (364), followed by Southwest, Northwest, and Northeast.

## Key Business Question and Insights

### 1. Does the gender of the person matter for the company as a constraint for extending policies?

![Screenshot 2025-03-22 220622](https://github.com/user-attachments/assets/87e47627-2784-419e-adad-261832ca7ec1)

#### Insight
- The boxplot shows that **gender does not significantly affect the insurance claim amounts**.
- Males and females have similar distributions, suggesting that gender should not be a constraint.

### 2. What is the average amount of money the company spent over each policy cover?

On average, the company spends Rs.13,270.4223 per policy cover. It helps us evaluate how efficiently our policies are priced and whether we need to optimize costs or adjust coverage plans.

### 3. Should the company need to offer separate policies based upon the geographic location of the person?

![Screenshot 2025-03-22 221156](https://github.com/user-attachments/assets/5a5c1fcc-fca7-4e71-ba8d-61438da513d3)

#### Insight
- The boxplot illustrates the variation in insurance charges across different geographic regions southwest, southeast, northeast, northwest. 
- Southeast regions shows a higher spread in insurance charges.
- All regions exhibit outliers, indicating that certain individuals are charged significantly higher than the average possibily due to smoking, high BMI(Body Mass Index), or other risk factors.
- **Geographic locations does not have a major impact on insurance charges.**

### 4. Does the no. of dependents make a difference in the amount claimed?

![Screenshot 2025-03-22 221826](https://github.com/user-attachments/assets/20c02ec8-d371-4cdc-9fb1-f30ea034f556)

#### Insight
- The boxplot illustrates the impact of number of dependents on insurance charges.
- The distribution remains similar across different numbers of dependents.
- There is **no strong trend indicating a direct impact of dependents on claim amounts**.

### 5. Does a study of persons BMI get the company any idea for the insurance claim that it would extend?

![image](https://github.com/user-attachments/assets/c619cda0-b5fc-441b-a7fe-eb4ca90fafc0)

#### Insight
- This scatter plot examines the **correlation between Body Mass Index (BMI) and insurance charges**.
- Each dot represents an individual, with BMI on the x-axis and insurance charges (INR) on the y-axis.
- A **positive trend** is observed, indicating that **higher BMI** is generally associated with **higher insurance costs**.

### 6. Is it needed for the company to understand whether the person covered is a smoker or a non-smoker?

![Screenshot 2025-03-22 223540](https://github.com/user-attachments/assets/7a0ad98f-00c9-454d-9eee-08101b5e11fb)

#### Insight
- This box plot highlights the **significant impact of smoking on insurance charges**.
- **Smokers** have considerably **higher median charges** compared to **non-smokers**.
- **Non-smokers** generally have lower insurance charges,
- **Smoking is a major risk factor influencing insurance premium**.

### 7. Does age have any barrier on the insurance claimed?

![Screenshot 2025-03-22 222305](https://github.com/user-attachments/assets/5b11f8b3-bbd6-4764-b2b6-41474f0483e1)
   
#### Insight
- **Left Chart (Box Plot):**
    - **Insurance charges tend to increase with age**, with older age groups showing a higher median.
    - The variability in charges is higher in older age groups, with more outliers at higher values.
    - Younger individuals (18-29) have the lowest median charges.

- **Right Chart (Scatter Plot):**
    - **Smokers (blue dots)** consistently face **higher charges** than **non-smokers (red dots)** across all age groups.
    - As age increases, both smokers and non-smokers see a rise in insurance costs, but the gap between smokers and non-smokers remains significant.
    - The trend suggests that **older smokers face the highest insurance charges.**

- **Aging leads to an increase in insurance charges, with smokers experiencing significantly higher costs compared to non-smokers at every age.**

### 8. Can the company extend certain discounts after checking the health status (BMI) in this case?

![Screenshot 2025-03-22 223557](https://github.com/user-attachments/assets/e3cff480-0998-4d17-9ee1-3c1788af70c0)

#### Insight
- **Higher BMI is associated with increased insurance charges.**
- The highest BMI category **(40-55)** has the widest spread in charges, indicating greater variability.
- **Individuals with lower BMI (below 25) tend to have lower claims. Offering discounts for healthier individuals could be a viable strategy.**


## Conclusion
- On average, the company spends Rs.13,270.4223 per policy cover.
- A **positive trend** is observed, indicating that **higher BMI** is generally associated with **higher insurance costs**.
- **Smoking is a major risk factor influencing insurance premium**.
- **Aging leads to an increase in insurance charges, with smokers experiencing significantly higher costs compared to non-smokers at every age.**
- **Individuals with lower BMI (below 25) tend to have lower claims. Offering discounts for healthier individuals could be a viable strategy.**



