# Technologies

<details>
  <summary>Links</summary>
  
  ## Portfolio Links
  - [Introduction](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Introduction.md "Introduction")  
  - [Requirements](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Requirements.md "Requirements")  
  - [Technologies](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Technologies.md "Technolgoies")  
  - [Approach](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Approach.md "Approach")  
  - [Risks & Challenges](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/RisksAndChallenges.md "Risks & Challenges")  
  - [Issues](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Issues.md "Issues")  
  ## External Links
  - [OpinionMarket](http://clientapp6-env.eba-sifj8dsx.us-west-1.elasticbeanstalk.com/ "OpinionMarket")  
  - [Swagger](https://app.swaggerhub.com/apis/JoshV3742/Capstone/1.0.0 "Swagger")  
</details>

###  Server-Side  
- Spring Boot 2.4.1
- MongoDB 4.2.10
- Github OAuth2

### Client-Side  
- React 16.13.1
- Redux 4.0.5
- Material-UI 4.11.0

### Cloud
- Docker
- AWS EC2
- AWS Elastic Beanstalk  

### Spring Boot
The decision to use Spring Boot was made after evaluating alternatives including .NET Core and Express. Proof of concept applications were built using each framework under consideration. Based on these proofs of concept, Spring Boot was determined to be the most suitable framework for the project due to the ease with which it can be containerized, deployed to clouds, and integrated with MongoDB. Spring Boot also offers the Netflix Eureka service discovery solution that was used to handle routing, the Maven package management tool that was used to automate testing and deployment, and the innovative annotation-driven library Project Lombok that significantly reduces the amount of boilerplate code in the project.  

### MongoDB
MongoDB was chosen because of its increasing popularity and innovative approach to data persistence. The JSON-like format in which Mongo documents are stored clarifies the structure of an object and eliminates the need for the complex joins often used with relational databases. Mongo can store objects within other objects using embedding, which represents a code object more accurately than relational databases can. In keeping with the theme of high scalability, MongoDB is designed to be easy to scale-out. Mongo does not use a schema. As a result, documents can take whatever form most precisely represents the relevant data, making the application more flexible. Because both microservice architecture and MongoDB increase an application’s scalability and flexibility, it makes sense to use them together.  

## Next 
[Approach](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Approach.md "Approach")

