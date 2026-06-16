
# Academic Program Transfer Planner

## Project Description
This web application assists a Computer Science student in evaluating a transfer to another academic program. The system displays transcript courses, allows selection of a target program, and generates an equivalency table for completed courses.

## Technologies Used
- HTML
- CSS
- JavaScript

## Current Program
**Computer Science**

## Implemented Features

### Course Table
The application automatically loads:
- Passed courses
- Failed courses
- Courses currently in progress
- Five additional Computer Science courses

### Program Selection
Available target programs:
1. Computer Engineering
2. Civil Engineering
3. Electrical and Electronics Engineering

### Transfer Function
After pressing the **Transfer** button:
- Only completed (passed) courses are processed.
- Equivalent courses are searched in the selected program.
- If no reasonable match exists, the application displays **N/A**.

## Equivalency Algorithm

### Overview
The algorithm uses predefined equivalency mappings based on course content similarity.

### Steps
1. Load all transcript courses.
2. Filter courses with status **Yes**.
3. Read the selected target program.
4. Compare each completed course with a mapping table.
5. Display the equivalent course if found.
6. Otherwise display **N/A**.

### Example

| Current Course | Equivalent Course |
|---------------|-------------------|
| Introduction to Programming | Introduction to Programming |
| Computer Organization | Computer Architecture |
| Basics of Physics I | Physics I |
| Computer and Society | N/A |

## System Design
The project contains:
- Course database (JavaScript array)
- Program-specific equivalency maps
- Dynamic table generation
- Event-driven transfer operation

# Future Improvements

## Automatic Syllabus Comparison with AI

The current implementation relies on manually defined mappings. A future version can automate equivalency detection.

### Proposed Algorithm

1. Load syllabus documents (PDF, DOCX).
2. Extract:
   - Course title
   - Learning outcomes
   - Topics
   - Credits
   - Prerequisites
3. Preprocess text:
   - Remove stop words
   - Normalize terminology
   - Extract keywords
4. Generate AI embeddings for every syllabus.
5. Calculate semantic similarity between courses.
6. Rank possible equivalents.
7. Generate an equivalency table automatically.
8. Provide a confidence score and explanation.

### Example Output

| Course A | Course B | Similarity |
|----------|----------|------------|
| Object Oriented Programming | OOP for Engineers | 92% |
| Operating Systems | System Software | 88% |

### Benefits
- Faster transfer evaluation
- Reduced manual work
- More objective comparison
- Ability to process hundreds of courses
- Transparent AI-based recommendations
- Better support for academic advisors
