# SMarTMaNNs Web Application 
## Introduction / Summary
* Main purpose of this project in current branch(<i>main branch</i>) is to design project structure, and to connect components(establishing linkages and relationships).
* (Thus,) Further implementation and tests for real application will be branched into private repository.
* Following stacks and topics are planned to be covered through this template-like project.
  * Spring Boot (framework, initializer, DI, ORM, DB connection, ...)
  * Kotlin (programming language)
  * Gradle (build tool)
  * RESTful API (design, paradigm)
  * Microservices (architecture, paradigm)
  * Web Application (program type, service style)
  * Apache Kafka (messaging system)
  * Apache Spark, PostgreSQL (databases)
  * Kubernetes (container platform; probably adapted to run microservices, databases, and messaging systems)
  * AWS (cloud service; highly considered as a runtime machine or a platform)
* Definition of system:
  * <b>Securities Firm API Client(a.k.a <i>Client</i>)</b> performs most of the transactions utilizing APIs provided by securities firms. <br>
    It is also responsible for credential operations and process both human and machine input like a terminal. <br>
    (features and its role will be gradually changed. See also the last paragraph about future considerations below.)
* Features to be achieved are as follows:
  * As web application; 
    * Provide APIs to access to the user data, of whom currently logged-in the client. 
    * Provide APIs to perform transactions of stocks and securities.
  * As back-end/microservices;
    * Real time update of DB(Apache Spark) using messaging system(Kafka) which is working like a data streaming pipeline.
    * For every operation(including market transactions), perform intact, and leave logs. Histories in the logs will be stored in DBs and would be cached.
    * Take responsibilities to deal with internal errors and integrate system(a bunch of our programs) components.
* Future considerations & long-term goals
  * Migrate non-essential portion of the client from current Python based program to Kotlin, <br>
    considering that it would be a controller instead of a full-scale program, focusing on its duty as an API controller.