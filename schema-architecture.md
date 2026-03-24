Section 1: Architecture summary
es both MVC and REST controllers. Thymeleaf templates are used for the Admin and Doctor dashboards, while REST APIs serve all other modules. The application interacts with two databases—MySQL (for patient, doctor, appointment, and admin data) and MongoDB (for prescriptions). All controllers route requests through a common service layer, which in turn delegates to the appropriate repositories. MySQL uses JPA entities while MongoDB uses document models.

Section 2: Numbered flow of data and control
1. User accesses AdminDashboard or Appointment pages.
2. The action is routed to the appropriate Thymeleaf or REST controller.
3. The controller calls the service layer
4. The service layer communicates with the Repository layer for data access operations
5. Each repository interact directly with the database engine such as Mysql and MongoDB
6. Data retrieved from the Database is mapped into Java model classes.
7. Models are passed from controller to Thymeleaf templates for the web and JSON for RESTFul apis 