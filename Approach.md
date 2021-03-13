# Approach

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

### Backend
<p>OpinionMarket leverages a **microservice architecture**. The application has been divided into several smaller applications that are designed around related functionality. Code bounderies seperate user functionality (authentication and profiles), community functionality (communities, posts, and comments), and conversation fucntionality (messaging).  This minimizes the number of users stories that require cross-service sagas. The **API Gateway** recevies all client requests and leverages the Eureka discovery service to perform **dynamic server-side service routing**. The gateway also handles **service orchestration** and **OAuth2** security.</p>  

<p>Each data microservice is designed with a **layered architecture**. The services are divided into API, Business logic, and data access/persistance layers. The API layer acts as a **facade** over the business logic of the applications. This layer concerns itself with validating and responding to requests. **The Data Transfer Object (DTO)** design pattern is used to encapsulate response data, messages, and status codes. The business logic layer handles all business rules and business logic including transforming data and overseeing database operations. There are no calls to other microservices in the business layer or in any layer. This is because service orchestration is handled in the API gateway. This approach keeps services loosly coupled and easy to maintain because sagas are defined in just one place in the system. The data access/persitance layer perfoms Create, Read, Update, and Delete (CRUD) operations on the service's database. No business logic is performes in the data access layer.</p>

### Frontend
The client application is 
