# Technologies

<details>
  <summary>Links</summary>
  
  ## Portfolio Links
  - [Introduction](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Introduction.md "Introduction")  
  - [Requirements](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Requirements.md "Requirements")  
  - [Technologies](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Technologies.md "Technolgoies")  
  - [Technical Approach](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Approach.md "Technical Approach")  
  - [Risks & Challenges](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/RisksAndChallenges.md "Risks & Challenges")  
  - [Issues](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Issues.md "Issues")  
  ## External Links
  - [OpinionMarket](http://clientapp6-env.eba-sifj8dsx.us-west-1.elasticbeanstalk.com/ "OpinionMarket")  
  - [Swagger](https://app.swaggerhub.com/apis/JoshV3742/Capstone/1.0.0 "Swagger")  
</details>

### Rationale
I selected technologies based on the following criteria:  
- **Each major technology must be new to me**
- Each technology should be industry-relevant
- All technologies should work well together
###  Server-Side  
- [Spring Boot 2.4.1](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Technologies.md#spring-boot "Spring Boot")
- [MongoDB 4.2.10](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Technologies.md#mongodb "MongoDB")
- [Maven 3.6.3](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Technologies.md#spring-boot "Spring Boot")

### Client-Side  
- [React 16.13.1](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Technologies.md#react-with-redux-and-material-ui "React")
- [Redux 4.0.5](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Technologies.md#react-with-redux-and-material-ui "React")
- [Material-UI 4.11.0](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Technologies.md#react-with-redux-and-material-ui "React")

### Cloud
- [Docker](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Technologies.md#docker "Docker")
- [AWS EC2](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Technologies.md#amazon-web-services-aws "AWS")
- [AWS Elastic Beanstalk](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Technologies.md#amazon-web-services-aws "AWS")

### Spring Boot
The decision to use **Spring Boot** was made after evaluating alternatives including .NET Core and Express. Proof of concept applications were built using each framework under consideration. Based on these proofs of concept, Spring Boot was determined to be the most suitable framework for the project due to the ease with which it can be **containerized**, deployed to clouds, integrated with **MongoDB**, and its compatibility with **microservice architecture**. Spring Boot offers the **Netflix Eureka service discovery** solution that was used to handle routing requests to microservices. In addition, Spring Boot easily integrates with the **Maven** package management tool that provides the plugins used to support **DevOps** capabilities such as **automated unit and integration testing** and **CI/CD pipelines**. The innovative annotation-driven library **Project Lombok**, available for Spring Boot, was leveraged to significantly reduce the amount of boilerplate code in the project.  

I chose to learn Spring Boot because of the ease with which it can be used to create Spring applications with opinionated configurations. Spring Boot makes writing code a breeze with its **annotation-driven features**, **database repositories**, and libraries that reduce boilerplate code.

### MongoDB
**MongoDB** was chosen because of its increasing popularity and innovative approach to data persistence. The JSON-like format in which Mongo documents are stored clarified the structure of objects and eliminated the need for the complex joins often used with relational databases. Mongo can store objects within other objects using **embedding**, which represents a code object more accurately than relational databases can. In keeping with the theme of high scalability, MongoDB is designed to be easy to **scale-out**. Mongo does not use a schema. As a result, documents can take whatever form most precisely represents the relevant data, making the application more flexible. Because both **microservice architecture** and MongoDB increase an application’s scalability and flexibility, it made sense to use them together.  

I chose to learn MongoDB because I had never worked with a **NoSQL** database before. I had worked with many relational databases such as PostgreSQL, MySQL, MariaDB, and Microsoft SQL Server and wanted to ensure my database engineering skills were well-rounded.

### React (with Redux and Material-UI)  
**React** was selected for use in the project because of its status as the most popular frontend framework. React provides several advantages including the ability to reuse HTML code across the application, a **virtual document object model (DOM)** that eliminates inefficiencies associated with the actual DOM, and the ability to use **Redux** for storing data that will be needed across the application. **Material-U**I was chosen as the application’s frontend CSS library because of the **responsive components** it provides, its extensive collection of beautiful UI elements, and its comprehensive official documentation.  

I chose to learn React because of the high demand for it in the industry. I choose to learn Redux because I wanted to be able to build React applications that effectively manage state. I choose to learn Material-UI because of the ease with which it can be used to add beautiful UI elements to components.

### Docker  
**Docker** was chosen as the container solution for OpinionMarket because it simplifies development and supports **DevOps**. **Docker containers** provided a consistent and isolated environment for applications to run in. As a result, productivity increased because developer time could be directed towards development instead of debugging complex environment issues. Using Docker with **microservice architecture** was a natural decision for several reasons, including increased application scalability and flexibility. Docker containers clearly defined the code boundaries between microservices, containers could be easily replaced when an update was needed without affecting other containers, and containers could be easily scaled in the cloud. Docker and **Docker Hub** were used as components of the application's **CI/CD pipeline**. **Maven** builds triggered automated Docker build and push operations. The open-source **Watchtower** project was leveraged to automatically and gracefully update the containers running on production **EC2** instances whenever a new version was available.

I chose to learn Docker because I had never done any application containerization before and wanted to understand the concept. I was also happy to take advantage of the predicatable environment containers provide to focus on application development.

### Amazon Web Services (AWS)
**AWS** was chosen because of the maturity of its services and its compatability with **microservice architecture**. AWS is the cloud solution of choice for microservice architecture according to the [State of Microservices](https://tsh.io/state-of-microservices/ "State of Microservices Report") report. AWS’s **Elastic Cloud Compute (EC2)** and **Elastic Beanstalk** services make deploying Docker containers as painless as possible. OpinionMarket’s backend microservices were deployed in EC2 containers, while the client application was deployed in Elastic Beanstalk. Because of its compatibility with **Docker** and with microservice architecture, AWS was a natural choice for the project’s cloud solution.

I chose to learn AWS because it is the most complete, mature, and innovative cloud provider in the industry. I was able to leverage both **Infrastructure-as-a-Service (IaaS)** and **Platform-as-a-Service (PaaS)** solutions from AWS. Having gained familiarity with AWS, I hope to add more services to my skill set in the near future including the Lambda servless solution.

## Next 
[Technical Approach](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Approach.md "Approach")

