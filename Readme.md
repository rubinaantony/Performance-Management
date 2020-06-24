__Get This Project__
===================

git clone --recurse-submodules https://github.com/rubinaantony/Performance-Management.git

__Performance Management__
===================


A web application that enables the administrator to provide performance evaluation for its employees. The administrator can also assign any employee to provide feedback on the performance evaluation result of another employee.


__E.g:__ The administrator can assign employee A to see the performance evaluation results of employee B. The employee A can then provide his feedback on the evaluation results of employee B. Employee A can specify if he agrees or disagrees with the evaluation result of employee B. However, the employee A cannot view his/her performance evaluation results published by the administrator.

The web application is designed using Angular (v8) and Spring Boot for the front end and back end respectively.

The user logs into the web application using his/her credentials. Based on their assigned role they are redirected to either the admin's or the employee's page. They also have an option for password recovery.


__Note__
```
The design incorporates H2 In-memory database to avoid the db setup during the project runtime and limited it to run during the dev profile alone
(spring.profiles.active = dev).

ServerHostName/h2-console can be used to check the table data at runtime.
```

The code for the Angular and Spring Boot part are separated and is available at

* [Angular](https://github.com/rubinaantony/Performance-Management-Angular)
* [Spring Boot](https://github.com/rubinaantony/Performance-Management-Spring)


### __User Capabilities__ ###
This section describes the capabilities for the administrator and employee user.

#### __Capabilities of the administrator__ ####

* Add/Update/Delete/View employee details
* Add/Update/View performance evaluation for the employees
* Assign an employee to provide feedback on the performance evaluation result of another employee


#### __Capabilities of the employee user__ ####


* View a list of employees towards which the user is assigned to provide feedback on their performance evaluation
* Provide feedback on the performance evaluation of other employees.

### __Assumptions Made__ ###
It is assumed that the administrator is the only user who is having complete control of what is provided into the system. Only the administrator can add or view the performance evaluation for all the employees. An employee cannot view his/her own performance evaluation results. He/She can only view the performance evaluation results of other employees and provide feedback towards that, if the administrator has assigned the employee to do so.

This way, this system can enable the administrator to understand if the employees of the company agrees with the performance evaluation provided by the administrator towards their colleagues and can take corrective actions.

### __Technologies Used__ ###
* Angular Version 8.2.14
* Node Version 12.13.1
* Spring Boot Version 2.3.1
* h2database Version 1.4.197
* Oracle Application Express (APEX)
* Java Version 1.8


### __APIs Used__ ###
* POST
* GET
* DELETE
* PUT


### __Dependencies Used__  ###
* [Spring Boot Starter Web](https://docs.spring.io/spring-boot/docs/2.2.2.RELEASE/reference/htmlsingle/#using-boot-starter)
* [Spring Data JPA](https://spring.io/guides/gs/accessing-data-jpa/)
* [Oracle Application Express](https://apex.oracle.com/en/learn/getting-started/)
* [H2 database](https://spring.io/guides/gs/accessing-data-jpa/)


### __Possible Improvements__ ###

The current design does not qualify to be of a production grade quality. Logging is not employed for any kind of detailed debugging. The design does not keep track of the user session and also have not implemented any spring security.


### __Author__ ### 
Rubina Brijith Antony
