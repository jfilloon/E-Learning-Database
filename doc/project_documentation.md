# Data Requirements 

## Features 
- Track Student Enrollment
- Track Course Participation
- Manage Assignments, Submissions, and Participation
- Attendance and Engagement Tracking
- Uses Normalized Relational Schema 
-----

## User Data 
### Student
- sid
- firstname
- lastname
- email
- dob
- edate

### Student
- iid
- firstname
- lastname
- email
- dept
  
------

## Course Data
### Course
- cid
- cname
- cdesc
- credits
- clevel

### Enrollment
- eid
- sid
- cid
- edate
- cstatus

-------

## Academic Activity Data
### Assignment
- aid
- cid
- atitle
- adesc
- duedate
- points

### Submission
- subid
- aid
- sid
- subdate
- sublink

### Grade
- gid
- subid
- score
- gletter
- feedback

--------

## Participation Tracking Data
### Attendance
- aid
- sid
- cid
- cdate
- attstatus

-----------







