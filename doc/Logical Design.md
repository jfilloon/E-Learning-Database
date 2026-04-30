# Logical Design

## Overview
This section converts the ER model into relational tables. Each table includes a primary key, foreign keys where needed, and basic constraints.

---

## Student
- sid (PK)
- firstname (NOT NULL)
- lastname (NOT NULL)
- email (UNIQUE, NOT NULL)
- dob
- edate (NOT NULL)

---

## Instructor
- iid (PK)
- firstname (NOT NULL)
- lastname (NOT NULL)
- email (UNIQUE, NOT NULL)
- dept (NOT NULL)

---

## Course
- cid (PK)
- iid (FK references Instructor.iid)
- cname (NOT NULL)
- cdesc
- credits (NOT NULL)
- clevel (NOT NULL)

---

## Enrollment
- eid (PK)
- sid (FK references Student.sid)
- cid (FK references Course.cid)
- edate (NOT NULL)
- cstatus (NOT NULL)

---

## Assignment
- aid (PK)
- cid (FK references Course.cid)
- atitle (NOT NULL)
- adesc
- duedate (NOT NULL)
- points (NOT NULL)

---

## Submission
- subid (PK)
- aid (FK references Assignment.aid)
- sid (FK references Student.sid)
- subdate (NOT NULL)
- sublink

---

## Grade
- gid (PK)
- subid (FK references Submission.subid)
- score (NOT NULL)
- gletter
- feedback

---

## Attendance
- attid (PK)
- sid (FK references Student.sid)
- cid (FK references Course.cid)
- cdate (NOT NULL)
- attstatus (NOT NULL)

---

## Constraints
- Student email must be unique.
- Instructor email must be unique.
- Credits must be greater than 0.
- Assignment points must be greater than 0.
- Grade score must be between 0 and the assignment points possible.
- Enrollment status should be limited to values such as Active, Completed, or Dropped.
- Attendance status should be limited to values such as Present, Absent, or Late.
