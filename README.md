# Personal Project Management Application


As well assumed by the name , this is a simple Personal Project Management Application.


Question :
    Let's say that the front end of your application is using ReactJS. How would you connect it to 
    the backend Java-Spring of your application ?
    
    Answer : 
    
    There are several ways to connect the frontend to the backend.However,what I did to implement this mechanism 
    here, was that I created the backend of the application first; then I create another directory consisting of 
    the frontend for the application.I deployed the Java-Spring app through heroku prior to deploying the frontend. 
    Once I got the heroku/production URL; I copied/pasted it within my 'package.json' file, in the frontend 
    repo/app of my application. 
                                         
                                         'proxy': ' heroku url '
    Whilst developing the frontend of my app, I also made sure to call the Spring REST API, from the ReactJS frontend, 
    using the **axios** framework, particularly within the 'backlogActions.js' file of my frontend app. Here is where
    you need to ensure that ALL of the actions are calling the ROUTE and not the host. 
        
        ex:
            try{
                  await axios.post(`/api/backlog/${backlog}`, project_task);
                  history.push(`/projectBoard/${backlog_id}`); 
                  dispatch({
                        type: GET_ERRORS,
                        payload: {}
                });
            
            
            
   Used technologies:

    Backend: Spring Boot.
      -Libraries: web, security, jjwt, gson, spring-data-JPA(Hibernate).
      -Build tool: Maven.
    Frontend: React 16.12
      -Libraries: redux-thunk, axios, classnames,jwt-decode
      -Build tool: npm.
    Database: MySQL, h2.
    

 
   Features:
    
    * Sign Up ( create an account )
    * Password Verification
    * Login & Logout
    * Create a Project(Task) to Manage
    * Give Project a unique ID and short description
    * Assign yourself a start date & presumed end date
    * Assign yourself tasks that need to be completed in order to complete the project
    * Set the status for each of your tasks (To Do, In Progress, Done)
    * Set the priority for each of your tasks (High, Medium , or Low) 
    * You can only see + edit projects that belong to you ( hence Personal Project Management )  
  
   
   

    
    
 
  

