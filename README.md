# MGNREGA
The Mahatma Gandhi National Rural Employment Gurantee Act(MGNREGA) is an Indian Law which gives gurantee rural areas by providing at least 100 days of guranteed wage employment .
a. BDO (Block Development Officer)

b. Gram Panchayat member

A project is created by BDO,which is assigned to corresponding Gram panchayat Members. Gram Panchayat member has acccess to assign to Employees to Complete the Project.<br/>

<!--![Flow Chart1](https://user-images.githubusercontent.com/80202600/223318909-240455f4-8989-4811-9f96-4d378f7b7667.jpg)-->


Features<br/>
BDO and GPM can login and logout.<br/>
BDO can create Project and GPM and provide their detail.<br/>
BDO can see the List of Project, GPM amd Employee's along with all the detail.<br/>
BDO can assign project to GPM amd GPM can assign to Employee.<br/>
GPM can see the list of Employee and Amount receivable till date according to daily wage.<br/>
GPM can only assingn only those project which are assign to them by BDO.<br/>
GPM can only assingn project to Employee.<br/>

<br/>
<h1>Click here to watch presentation video<a href="https://drive.google.com/drive/folders/1goR-namqIyvzPJDyHdRgEKMNwRL9n7mx" target=_blank>Link</a></h1>
Used Tech stacks and Tools<br/>
Java<br/>
MySQL<br/>
Git & GitHub<br/>
JDBC<br/>

<br/>
mysql> desc bdo;
<br/>
| Field    | Type        | Null | Key | Default | Extra | <br/>
|:-----:
| id       | int         | NO   | PRI | NULL    |       | <br/>
| username | varchar(20) | NO   |     | NULL    |       | <br/>
| password | varchar(20) | YES  |     | NULL    |       | <br/>
| location | varchar(20) | YES  |     | NULL    |       | <br/>
| email    | varchar(20) | YES  |     | NULL    |       | <br/>
<br/>
5 rows in set (0.07 sec)
<br/>
mysql> desc employee;
<br/>
| Field    | Type        | Null | Key | Default | Extra |<br/>
| :----:   |:----------:
| empid    | int         | NO   | PRI | NULL    |       |<br/>
| ename    | varchar(20) | YES  |     | NULL    |       |<br/>
| age      | int         | YES  |     | NULL    |       |<br/>
| location | varchar(20) | YES  |     | NULL    |       |<br/>
| wages    | int         | YES  |     | NULL    |       |<br/>
| mobilno  | varchar(20) | YES  |     | NULL    |       |<br/>
| pid      | int         | YES  | MUL | NULL    |       |<br/>
| days     | int         | YES  |     | NULL    |       |<br/>
<br/>
8 rows in set (0.01 sec)
<br/>
mysql> desc eproj;
<br/>
| Field  | Type | Null | Key | Default | Extra |<br/>

| emp_id | int  | YES  | MUL | NULL    |       |<br/>
| p_id   | int  | YES  | MUL | NULL    |       |<br/>
<br/>
2 rows in set (0.01 sec)
<br/>
mysql> desc gpm;
<br/>
| Field    | Type        | Null | Key | Default | Extra |<br/>

| gpmid    | int         | NO   | PRI | NULL    |       |<br/>
| name     | varchar(20) | YES  |     | NULL    |       |<br/>
| email    | varchar(20) | YES  |     | NULL    |       |<br/>
| password | varchar(20) | YES  |     | NULL    |       |<br/>
| location | varchar(20) | YES  |     | NULL    |       |<br/>
| mobilno  | varchar(20) | YES  |     | NULL    |       |<br/><br/>
| prid     | int         | YES  | MUL | NULL    |       |<br/>
<br/>
7 rows in set (0.01 sec)
<br/>
mysql> desc project;
<br/>
| Field    | Type        | Null | Key | Default | Extra |<br/>

| projid   | int         | NO   | PRI | NULL    |       |<br/>
| name     | varchar(20) | YES  |     | NULL    |       |<br/>
| projdesc | varchar(20) | YES  |     | NULL    |       |<br/>
| date     | date        | YES  |     | NULL    |       |<br/>
| duration | int         | YES  |     | NULL    |       |<br/>

5 rows in set (0.01 sec)
