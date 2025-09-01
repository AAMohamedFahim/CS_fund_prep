# Keys in Relational Model - Short Technical Notes

## Concept: Super Key
**Definition:** A set of one or more attributes that uniquely identify a tuple, possibly containing extra unnecessary attributes.  
**Key Points:**  
- Uniquely identifies rows in a table, may have extra attributes.  
- Supports NULL values in rows.  
- Example: STUD_NO or (STUD_NO, SNAME) in a STUDENT table.  
**Example (optional):** Combination of STUD_NO and PHONE uniquely identifies a student.

## Concept: Candidate Key
**Definition:** A minimal super key with no extra attributes that uniquely identifies a record.  
**Key Points:**  
- Minimal set of attributes ensuring uniqueness.  
- Every table must have at least one candidate key.  
- Multiple candidate keys can exist but only one becomes the primary key.  
**Example (optional):** STUD_NO uniquely identifying each student in STUDENT table; {STUD_NO, COURSE_NO} in STUDENT_COURSE table.

## Concept: Primary Key
**Definition:** Chosen candidate key that uniquely identifies each record and cannot be NULL.  
**Key Points:**  
- Must have unique values, no duplicates allowed.  
- Cannot be NULL for any record.  
- Can be a single or composite key.  
- Databases often use primary key ordering for fast access.  
**Example (optional):** STUD_NO as primary key in STUDENT table.

## Concept: Alternate Key
**Definition:** Candidate keys not selected as the primary key.  
**Key Points:**  
- Also called secondary keys.  
- Uniquely identify records but are not primary keys.  
- Can be single or composite keys.  
**Example (optional):** PHONE is an alternate key if STUD_NO is primary key in STUDENT table.

## Concept: Foreign Key
**Definition:** An attribute in one table that refers to the primary key in another table, creating a relationship.  
**Key Points:**  
- Establishes relationships between tables.  
- Helps maintain referential integrity and avoid redundancy.  
- Can contain NULL and duplicate values.  
**Example (optional):** STUD_NO in STUDENT_COURSE referencing STUD_NO in STUDENT table.

## Concept: Composite Key
**Definition:** Combination of two or more attributes to uniquely identify a record when no single attribute suffices.  
**Key Points:**  
- Acts as a primary key if no single key exists.  
- Accuracy depends on the attribute combination.  
- May still have rare duplicates if not optimally chosen.  
**Example (optional):** {STUD_NO, COURSE_NO} in STUDENT_COURSE table.
