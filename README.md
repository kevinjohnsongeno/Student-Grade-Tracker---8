# Grade Tracker SQL Procedures & Functions

This document provides an overview of how **CREATE PROCEDURE** and **CREATE FUNCTION** are applied in the Grade Tracker system to efficiently manage student marks, calculate totals, and ensure data integrity through conditional checks.

---

## Purpose

- Used **CREATE FUNCTION** to encapsulate reusable logic, such as verifying the existence of a subject before inserting marks.  
- Used **CREATE PROCEDURE** to handle complex operations like inserting student marks with calculated totals while enforcing business rules.  
- Applied **parameters and conditional logic** to make procedures and functions flexible and robust against invalid data inputs.  

---

## Use

1. **Validation with Functions**  
   - The function `isSubject()` checks if a subject code exists in the system, enabling conditional processing in procedures.  

2. **Safe Data Insertion**  
   - The procedure `insertMarks()` inserts marks only if the subject exists, calculating total marks automatically and preventing erroneous inserts.  

3. **Modularity and Reusability**  
   - Encapsulating subject validation in a function allows reuse in multiple procedures or queries without duplicating logic.  

4. **Error Handling**  
   - The procedure returns an informative message if an invalid subject code is provided, improving system robustness and user feedback.  

---

## Outcome

- **Maintain data integrity** by preventing invalid subject codes from being inserted.  
- **Simplify mark entry** with automatic total calculation and encapsulated validation logic.  
- **Promote reusable SQL logic** through functions and procedures that can be called consistently across the system.  
- **Enhance maintainability** by centralizing validation and business rules in database objects.  
