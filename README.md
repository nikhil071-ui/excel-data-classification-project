# HR Data Classification Project (Excel)

This project demonstrates the use of advanced Excel formulas to apply business logic and classify raw data.

## The Task
I was given an Excel file with employee compensation data, which included a 'Factory', 'Job Role', and an 'Equality Score'.

The goal was to create a new 'Equality class' column based on the following rules:
* **Fair:** Score is between -10 and +10
* **Unfair:** Score is less than -10 or greater than 10
* **Highly Discriminative:** Score is less than -20 or greater than 20

## My Solution
To solve this, I used a nested `IF` formula in Excel. The key was to check for the most extreme condition first (Highly Discriminative) and work down to the least extreme (Fair).

This ensures that a score of -25 is correctly marked as "Highly Discriminative" and not just "Unfair".

### The Formula
Here is the exact formula I used:

excel
=IF(ABS(C2)>20, "Highly Discriminative", IF(ABS(C2)>10, "Unfair", "Fair"))

BEFORE:
<img width="1918" height="1073" alt="Screenshot 2025-11-07 224252" src="https://github.com/user-attachments/assets/99bd2020-9b77-4e90-ac8b-88fd824fbcf6" />

AFTER:
<img width="1919" height="1079" alt="Screenshot 2025-11-07 224335" src="https://github.com/user-attachments/assets/b3c78d3b-1293-4837-9a0a-539ac58788b6" />

