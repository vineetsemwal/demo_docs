
***Microservices task***

***A University wants to manage the projects assigned to the students, Please write a microservices application for the same, User stories are given below along with basic desired skeleton ***

***Spring Boot, microservices (use discovery server) , SpringDataJpa JpaRepositories***


**User Stories**

1)Add Project in the system

2)Find project by id

3)Add Student

4) find student by id

5)Assign Project to Student

6)UnAssign project for a Student
  
  



**Student module**

Student{

id: long

name: String

field: String

age: Integer

 projects: List<Long>

}


IStudentRepository{

// add desired methods

......

}



IStudentService{

add(AddStudentRequest requestData) : StudentDetails

/** find student in the store by id **/ 

findStudentDetailsById(long id) :StudentDetails

/** find students by field **/ 

List< StudentDetails > findByField(String field)

void assignProject(AssignProjectRequest request) 

void unAssignProject(UnAssignProject request)

}



**Validations**

 id can't be null  or negative

name: min 2 letters, max 10 letters

field : 3 letters only

id, age can't be negative, age sgould be between 17 and 22





  **Project module**

  
  Project{
  
  id:long
  
  projectName:String

  description: String
    
  }

 IProjectRepository{

// add desired methods
 
 ...
 
 }
 
 IProjectService{
 
  add(AddProjectRequest request):ProjectDetails
 
  findProjectDetailsById(long id): ProjectDetails
 
 }
 
   
  **Validations**

id can't be null  or negative

name: min 2 letters, max 20 letters

description: min 2 letters, max 100 letters

