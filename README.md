# Smart Student Ranking and Search System

### Language & Algorithms

**Language:** C
**Algorithms:** Selection Sort, Insertion Sort, Binary Search
**Data Structure:** Array of Structures

A menu-driven C application for managing student records, generating rank lists, comparing sorting algorithms, and searching student records efficiently using Binary Search.

---

## Table of Contents

* [About the Project](#about-the-project)
* [Problem Statement](#problem-statement)
* [Module and Learning Objectives](#module-and-learning-objectives)
* [Functional Requirements](#functional-requirements)
* [Features](#features)
* [How the Algorithms Are Used](#how-the-algorithms-are-used)
* [Input and Output](#input-and-output)
* [Algorithm Complexity](#algorithm-complexity)
* [Getting Started](#getting-started)
* [Menu Options](#menu-options)
* [Performance Analysis](#performance-analysis)
* [Sample Demonstration](#sample-demonstration)
* [Team Members](#team-members)
* [Project File](#project-file)

---

## About the Project

The **Smart Student Ranking and Search System** is a console-based C application designed to manage student academic records and demonstrate fundamental searching and sorting algorithms.

Each student record contains:

| Field           | Description                       |
| --------------- | --------------------------------- |
| Roll Number     | Unique student identifier         |
| Name            | Student's full name               |
| Mathematics     | Marks obtained                    |
| Physics         | Marks obtained                    |
| Chemistry       | Marks obtained                    |
| Data Structures | Marks obtained                    |
| C Programming   | Marks obtained                    |
| Total           | Sum of marks in all five subjects |

The application allows users to:

* Add student records
* Edit existing student records
* Display all students
* Generate rank lists using Selection Sort and Insertion Sort
* Search students using Binary Search
* Compare sorting performance
* Analyze algorithm performance for different data arrangements and sizes

The program supports up to **100 student records**.

---

## Problem Statement

### Smart Student Ranking and Search System

Develop a console-based student record management application that demonstrates the use of **sorting and searching algorithms** on structured student data.

The system should allow users to store student records containing roll number, name, marks in five subjects, and total marks.

The application must provide functionality to:

1. Add and edit student records.
2. Display all stored student records.
3. Generate student rankings using Selection Sort and Insertion Sort.
4. Compare the number of comparisons, swaps, and shifts performed by the two sorting algorithms.
5. Search for a student using Binary Search based on roll number.
6. Analyze sorting performance using sorted, reverse-sorted, and random test data.

This project demonstrates how fundamental algorithms can be applied to a practical student record management problem.

---

## Module and Learning Objectives

### Module: Sorting and Searching Algorithms

The project focuses on:

* Understanding Selection Sort.
* Understanding Insertion Sort.
* Understanding Binary Search.
* Applying sorting algorithms to structured records.
* Generating student rank lists based on total marks.
* Comparing sorting algorithms using performance counters.
* Understanding best, average, and worst-case complexity.
* Understanding why Binary Search requires sorted data.
* Observing how input arrangement affects sorting performance.

The project also demonstrates the practical use of **structures, arrays, functions, recursion-free sorting, and algorithm-performance analysis in C**.

---

## Functional Requirements

The application satisfies the following requirements:

* Store up to 100 student records.
* Store roll number, name, five subject marks, and total marks.
* Allow users to add new students.
* Allow users to edit existing student records using roll number.
* Display all student records in tabular form.
* Generate rankings in ascending or descending order of total marks.
* Implement Selection Sort for ranking.
* Implement Insertion Sort for ranking.
* Count comparisons and swaps for Selection Sort.
* Count comparisons and shifts for Insertion Sort.
* Search student records using Binary Search.
* Automatically sort a copy of records by roll number before Binary Search.
* Generate sorted, reverse-sorted, and random test data.
* Analyze algorithm performance for different input sizes.

---

## Features

### 1. Student Record Management

Users can add student records containing:

* Roll Number
* Full Name
* Mathematics Marks
* Physics Marks
* Chemistry Marks
* Data Structures Marks
* C Programming Marks

The total marks are automatically calculated from the five subjects.

### 2. Edit Student Records

Existing records can be updated by entering the student's roll number.

The user can modify:

* Student name
* Marks in all five subjects

The total marks are recalculated automatically after editing.

### 3. Display Student Records

All stored records are displayed in a structured table containing:

* Roll Number
* Name
* Subject-wise marks
* Total marks

### 4. Student Ranking

The system generates rankings using two sorting algorithms:

* Selection Sort
* Insertion Sort

The ranking can be displayed in:

* Ascending order
* Descending order

The program also displays the performance statistics of both algorithms.

### 5. Student Search

The system searches for students using their roll number.

Before performing Binary Search, a copy of the student records is sorted by roll number. Binary Search is then applied to the sorted data.

The program reports the number of comparisons performed during the search.

### 6. Sorting Performance Analysis

The application compares Selection Sort and Insertion Sort using:

* Number of comparisons
* Number of swaps
* Number of shifts

The analysis is performed using different input sizes and data arrangements.

---

## How the Algorithms Are Used

### Selection Sort

Selection Sort is used to generate the student ranking based on total marks.

For every position in the array:

1. The algorithm searches for the appropriate minimum or maximum value.
2. The selected student is placed at the correct position.
3. The process continues until all students are sorted.

The program counts the number of comparisons and swaps performed.

---

### Insertion Sort

Insertion Sort is also used to generate the student ranking.

The algorithm:

1. Takes one student record at a time.
2. Compares it with previously sorted records.
3. Shifts larger or smaller records as required.
4. Inserts the current record into its correct position.

The program counts comparisons and shifts performed during sorting.

---

### Binary Search

Binary Search is used to find a student by roll number.

Since Binary Search requires sorted data, the program first sorts a copy of the student records by roll number using an insertion-sort-style process.

Binary Search then repeatedly divides the search range into two parts until the required roll number is found or the search range becomes empty.

---

## Algorithm Complexity

| Algorithm           | Best Case | Average Case | Worst Case |
| ------------------- | --------: | -----------: | ---------: |
| Selection Sort      |     O(n²) |        O(n²) |      O(n²) |
| Insertion Sort      |      O(n) |        O(n²) |      O(n²) |
| Binary Search       |      O(1) |     O(log n) |   O(log n) |
| Sort by Roll Number |      O(n) |        O(n²) |      O(n²) |

### Space Complexity

The sorting algorithms operate on arrays of student structures.

* Selection Sort: **O(1)** additional sorting space
* Insertion Sort: **O(1)** additional sorting space
* Binary Search: **O(1)** additional search space

The program also creates copies of the student array when comparing sorting algorithms and performing searches.

---

## Input and Output

### Input

The program accepts:

* Number of student records
* Student roll number
* Student name
* Marks for five subjects
* Ranking order
* Roll number for searching
* Menu selection

The five subjects are:

1. Mathematics
2. Physics
3. Chemistry
4. Data Structures
5. C Programming

### Output

The program displays:

* Student records
* Total marks
* Rank lists
* Selection Sort comparisons and swaps
* Insertion Sort comparisons and shifts
* Student search results
* Binary Search comparison count
* Sorting performance analysis

---

## Getting Started

### Prerequisites

Install a C compiler such as:

* GCC / MinGW on Windows
* GCC on Linux
* Clang on macOS

### Compile

From the project directory, run:

```bash
gcc student_ranking_search.c -o student_ranking_search
```

### Run on Windows PowerShell

```powershell
.\student_ranking_search
```

### Run on Linux or macOS

```bash
./student_ranking_search
```

---

## Menu Options

| Option | Operation                                           |
| ------ | --------------------------------------------------- |
| 1      | Add Student                                         |
| 2      | Edit Student                                        |
| 3      | Display All Students                                |
| 4      | Sort & Rank using Selection Sort and Insertion Sort |
| 5      | Search Student using Binary Search                  |
| 6      | Analyze Sorting Performance                         |
| 7      | Exit                                                |

The menu is implemented as a continuous loop until the user selects the Exit option.

---

## Performance Analysis

The performance analyzer compares Selection Sort and Insertion Sort using different input sizes:

```text
5
10
20
50
```

For each size, the program tests three types of data arrangements:

1. Already Sorted
2. Reverse Sorted
3. Random Order

The following metrics are recorded:

| Metric      | Selection Sort | Insertion Sort |
| ----------- | -------------- | -------------- |
| Comparisons | Yes            | Yes            |
| Swaps       | Yes            | No             |
| Shifts      | No             | Yes            |

The program uses generated test data to observe how the amount of work changes as the number of records increases.

### Expected Observations

* Selection Sort performs a similar number of comparisons regardless of the initial arrangement.
* Insertion Sort performs fewer shifts when the data is already sorted.
* Reverse-sorted data causes more shifting for Insertion Sort.
* The amount of work generally increases as the input size increases.

---

## Sample Demonstration

A typical execution can follow this flow:

```text
1. Add Student
       ↓
2. Edit Student (if required)
       ↓
3. Display All Students
       ↓
4. Sort & Rank
       ↓
   Selection Sort
       +
   Insertion Sort
       ↓
   Compare Performance
       ↓
5. Search Student
       ↓
   Binary Search
       ↓
6. Analyze Sorting Performance
       ↓
7. Exit
```

### Ranking Output

The ranking section displays two separate results:

```text
--- Rank List (Selection Sort) ---

Student Records...

Comparisons: ...
Swaps: ...

--- Rank List (Insertion Sort) ---

Student Records...

Comparisons: ...
Shifts: ...
```

The program also displays the topper's:

* Roll Number
* Name
* Total Marks

---

## Performance Metrics

### Selection Sort

**Comparisons:**
Number of times student totals are compared while finding the appropriate position.

**Swaps:**
Number of actual student-record exchanges performed.

### Insertion Sort

**Comparisons:**
Number of comparisons made while finding the correct position for each record.

**Shifts:**
Number of times a student record is moved to make space for the current record.

### Binary Search

**Comparisons:**
Number of roll-number comparisons performed while searching for a student.

---

## Project Structure

```text
Student-Ranking-and-Search/
│
├── student_ranking_search.c
└── README.md
```

---

## Team Members

| No. | Name            | Roll Number |
| --- | --------------- | ----------- |
| 1   | Ayush Ambetkar  | 25102A0025  |
| 2   | Omkar Menge     | 25102A0002  |
| 3   | Sandesh Jangale | 25102A0001  |
| 4   | Soham Bhabal    | 25102A0008  |

---

## Project File

```text
student_ranking_search.c
```

The complete application is implemented in a single C source file.

---

## Conclusion

The **Smart Student Ranking and Search System** demonstrates the practical implementation of fundamental **sorting and searching algorithms** using student records.

The project provides a practical comparison between **Selection Sort and Insertion Sort**, while **Binary Search** demonstrates efficient searching on sorted data.

It also provides performance analysis using different input sizes and data arrangements, helping demonstrate how algorithm efficiency changes with the nature and size of the input.

---

## Learning Outcome

Through this project, we gain practical understanding of:

* C structures
* Arrays of structures
* Functions
* Sorting algorithms
* Searching algorithms
* Selection Sort
* Insertion Sort
* Binary Search
* Algorithm complexity
* Performance measurement
* Student record management
* Menu-driven programming

---
