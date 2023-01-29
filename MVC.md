# SpringBoot-tutorials

<B>MVC(Model, View , Controller)<br></B>
Whenever Client sends a request , controller receives it and fetches the data from a model. The data is not in a presentable form and cannot be sent to the client directly, so it sends the data received to the view to make it presentable. The final response is then sent to the client.

<B>Annotations:<br></B>
<B>@Component<br></B>
We annotate all the classes that we want to create of object of with @Component, On running the Spring Boot application by default all the beans(objects) are created in the container, but only of the classes that are marked with @Component annotation.

<B>@Autowired</B>
If a class uses object of another class, we put @Autowired annotation above that object. This is because whenever SpringBoot application runs, the beans(objects) of all the component classes are generated, but the class that is using the object of another class does not know whether that object is present or not.
For example there is a class called College that uses a student class object
<br>
<B>@Component<br></B>
public class College
{<br>
<B>@Autowired<br></B>
Student student;<br>
//some lines of code<br>
}<br>
<br>
<B>@Component<br></B>
public class Student<br>
 {<br>
 //some lines of code<br>
 }<br>
 
Now whenever you run the main application, beans of College class and Student class will be generated. And the College class will know that a bean of  Student class exists.



