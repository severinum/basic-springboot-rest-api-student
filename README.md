# Basic Spring Boot Rest Api [Student]

This is very basic Spring Boot Rest Api that only have one entity - Student. It uses Postresql db (can be changed to any other in application.properties file
don't fotget to add correct dependencies in pom.xml file)

## Endpoints

1. **GET /api/v1/student**

This is the most obvious endpoint. It gets all students from the DB and returns it as JSON output

2. **POST /api/v1/student**

This one adding new Student to the DB. However it requires some body passed with this request. It should be JSON . For example: 
<pre>
  {
    "name": "Adam",
    "email": "adam.doe@myemail.com",
    "dob": "1980-09-11"
  }
 </pre>
 
 3. **DELETE /api/v1/student/{studentId}**
 
 This one will delete student (if student exists in the DB). Param: studentId should be a numeric [integer] value. For example /api/v1/student/4 [this one
 removes student with id 4]
 
 4. **PUT /api/v1/student/5?name={name_val_here}&email={email_val_here}**
 
 This one will update student with ID 5. Params 'name' and 'email' are optional. Both can exists in the url, none or one of them. 
 example : /api/v1/student/5?name=Theodore&email=teddy_funtasticone\\@teddymail.com
