Step1: sql below creates the view

ALTER 
ALGORITHM=UNDEFINED 
DEFINER=`root`@`localhost` 
SQL SECURITY DEFINER 
VIEW `view_demo` AS 
SELECT
	tbl_student.sid,
	tbl_student.`name`,
	tbl_course.course,
	tbl_phone.phone
FROM
	tbl_student
LEFT JOIN tbl_phone ON tbl_student.sid = tbl_phone.sid
LEFT JOIN tbl_course ON tbl_student.sid = tbl_course.sid ;

Step2: change the field name in above sql according to your need, all the data comes to single view table
Step3: once view is created write simple select query to get data in your code using the view table you have created above
