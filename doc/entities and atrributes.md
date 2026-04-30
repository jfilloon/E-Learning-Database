# Step 3: Entities and Attributes

## Overview
This section identifies the main entities in the e-learning platform database and lists the attributes for each entity.

---

## Student
- sid (PK)
- firstname
- lastname
- email
- dob
- edate

---

## Instructor
- iid (PK)
- firstname
- lastname
- email
- dept

---

## Course
- cid (PK)
- iid (FK)
- cname
- cdesc
- credits
- clevel

---

## Enrollment
- eid (PK)
- sid (FK)
- cid (FK)
- edate
- cstatus

---

## Assignment
- aid (PK)
- cid (FK)
- atitle
- adesc
- duedate
- points

---

## Submission
- subid (PK)
- aid (FK)
- sid (FK)
- subdate
- sublink

---

## Grade
- gid (PK)
- subid (FK)
- score
- gletter
- feedback

---

## Attendance
- attid (PK)
- sid (FK)
- cid (FK)
- cdate
- attstatus
