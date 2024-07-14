Building a Command-Line Course Manager for Krimson Kourses
==========================================================


1\. Add a Course

The input to add a course will be:

ADD_COURSE NAME <Course Name> SEQUENCE <Course Sequence>

 <Course Name> can contain multiple words and numbers.

 <Course Sequence> should be a number greater than or equal to 1. 

Do not add the course if the <Course Sequence>  is not a number, or is less than 1, or contains space in between. In this case, print: COURSE_SEQUENCE_NOT_VALID

Do not add if a course with the same name already exists

In this case, print: COURSE_NAME_ALREADY_EXIST

Do not add the course if the provided sequence already exists.

In this case, print: COURSE_SEQUENCE_ALREADY_EXIST

To add a course, the previous sequence should already be present. For example, the application should not add course 3 if courses 1 and 2 do not exist. In this case, print: ADD_COURSE_IN_SEQUENCE

If the pattern of the input is not valid, print:  REQUEST_PATTERN_INVALID

If the course is added successfully, print: SUCCESS

If there are multiple possibilities in the command, print only the error with the highest priority. The priority of errors is as follows:

REQUEST_PATTERN_INVALID

COURSE_SEQUENCE_NOT_VALID

COURSE_NAME_ALREADY_EXIST

COURSE_SEQUENCE_ALREADY_EXIST

ADD_COURSE_IN_SEQUENCE

2\. Add a Student

The input to add a student will be:

ADD_STUDENT NAME <Student Name> ID <Student ID>

 <Student ID>. should be a number greater than or equal to 0. If not, print: STUDENT_ID_NOT_VALID

Different students with the same name can exist, but the ID should be unique.

If a student with  <Student ID> already exists, print:  STUDENT_ID_ALREADY_EXIST

If the student is added successfully, print: SUCCESS

If the pattern of the input is not valid, print: REQUEST_PATTERN_INVALID

If there are multiple errors in the command, print only the error with the highest priority. The priority of errors is as follows:

REQUEST_PATTERN_INVALID

STUDENT_ID_NOT_VALID

STUDENT_ID_ALREADY_EXIST

3\. Assign Course to Student

The input to assign a course to a student will be:

COURSE_ASSIGN STUDENT <Student ID> COURSE <Course Sequence>

 <Course Sequence> should be a number greater than or equal to 1. If not, print: COURSE_SEQUENCE_NOT_VALID

 <Student ID> should be a number greater than or equal to 0. If not, print: STUDENT_ID_NOT_VALID

If <Course Sequence>   doesn't exist, print: COURSE_NOT_EXIST

If <Student ID> does not exist, print: STUDENT_NOT_EXIST

A course cannot be assigned to a student if the previous courses are not assigned. For example, the application should not assign course 6 if courses 1 to 5 are not assigned to that student. Courses should be assigned in sequence. Otherwise, print: PRE_REQUISITES_NOT_COMPLETED

If a student is already assigned the course or later courses, print: COURSE_ALREADY_ASSIGNED

If the course is assigned to the student successfully, print: SUCCESS

If the pattern of the input is not valid, print: REQUEST_PATTERN_INVALID

If there are multiple errors in the command, print only the error with the highest priority. The priority of errors is as follows:

REQUEST_PATTERN_INVALID

STUDENT_ID_NOT_VALID

COURSE_SEQUENCE_NOT_VALID

STUDENT_NOT_EXIST

COURSE_NOT_EXIST

PRE_REQUISITES_NOT_COMPLETED

COURSE_ALREADY_ASSIGNED

4\. Print Student Details

The input to get details will be:

STUDENT_DETAIL <Student ID>

 <Student ID> should be a number greater than or equal to 0. If not, print: STUDENT_ID_NOT_VALID

If the student doesn't exist, print: STUDENT_NOT_EXIST

If the command is valid, then print:

Name: <Student Name> 

ID: <Student ID>

Course Count: <Course Count>

 <Course Count> should be 0 if no courses are assigned yet.

If the pattern of the input is not valid, print: REQUEST_PATTERN_INVALID

If there are multiple errors in the command, print only the error with the highest priority. The priority of errors is as follows:

REQUEST_PATTERN_INVALID

STUDENT_ID_NOT_VALID

STUDENT_NOT_EXIST

5\. Print Course Details

The input to get details will be:

COURSE_DETAILS <Course Sequence>

<Course Sequence> should be a number greater than or equal to 1. If not, print: COURSE_SEQUENCE_NOT_VALID

If the course doesn't exist, print: COURSE_NOT_EXIST

If the command is valid, then print:

Name: <Course Name>

Sequence: <Course Sequence>

If the pattern of the input is not valid, print: REQUEST_PATTERN_INVALID

If there are multiple errors in the command, print only the error with the highest priority. The priority of errors is as follows:

REQUEST_PATTERN_INVALID

COURSE_SEQUENCE_NOT_VALID

COURSE_NOT_EXIST

6\. Exit The Application

The input to exit the application will be:

EXIT

Before exiting the application, print the following three lines:

Course Count: <Course Count>

Student Count: <Student Count>

Adios!

The default values for <Course Count> and <Student Count> are 0 if no course or student is added.

If there is extra information in the input, print: REQUEST_PATTERN_INVALID

7\. Unsupported Command

If the input starts with any other flag, then print: REQUEST_NOT_SUPPORTED

Here are a few examples of the same:

GET_SYLLABUS

ADD TEACHER

ADEXIT

ADDEXIT

ASSIGN EXIT ADD STUDENT NAME Iron Man ID 11.
