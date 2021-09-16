# Web App Security

## Hibernate Many to Many

Simple Entity Relationship Diagram:



The model classes Employee and Project need to be created with JPA annotations:

     @Entity
     @Table(name = "Employee")
     public class Employee { 
     // ...
 
     @ManyToMany(cascade = { CascadeType.ALL })
     @JoinTable(
        name = "Employee_Project", 
        joinColumns = { @JoinColumn(name = "employee_id") }, 
        inverseJoinColumns = { @JoinColumn(name = "project_id") }
     )
     Set<Project> projects = new HashSet<>();
   
     // standard constructor/getters/setters
     }
>

     @Entity
     @Table(name = "Project")
     public class Project {    
     // ...  
 
     @ManyToMany(mappedBy = "projects")
      private Set<Employee> employees = new HashSet<>();
    
     // standard constructors/getters/setters   
     }     

The @ManyToMany annotation is used in both classes to create the many-to-many relationship between the entities.