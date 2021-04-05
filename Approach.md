# Technical Approach

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

### Backend
OpinionMarket leverages a **microservice architecture**. The application has been divided into several smaller applications that are designed around related functionality. Code boundaries separate user functionality (authentication and profiles), community functionality (communities, posts, and comments), and conversation functoinality (messaging).  This minimizes the number of user stories that require cross-service **sagas**. The **API Gateway** receives all client requests and leverages the **Eureka discovery service** to perform **dynamic server-side routing**. The gateway also handles **service orchestration** and **OAuth2** authorization. If a request received by the gateway will require write operations in different databases, the gateway knows what **compensation transcation(s)** to perform in the event of a failure at any point in the saga. 

Each microservice is designed with a **layered architecture**. The services are divided into **API**, **business logic**, and **data access/persistance layers**. The API layer acts as a **facade** over the business logic of the application. This layer concerns itself with validating and responding to requests. **The Data Transfer Object (DTO)** design pattern is used to encapsulate response data, messages, and status codes. The business logic layer handles all business rules and business logic including transforming data and overseeing database operations. **Design by contract** and **dependency injection (DI)** are used to keep code maintainable. There are no calls to other microservices in the business layer or in any layer. This is because service orchestration is handled in the API gateway. This approach keeps services loosly coupled and easy to maintain because sagas are defined in just one place in the system. The data access/persitance layer perfoms **Create, Read, Update, and Delete (CRUD)** operations on the service's database. No business logic is performed in the data access layer.

### Frontend
The client application is built using **React** along with serveral common dependencies including **Redux** for state management, **Material-UI** for styling, **Axios** for HTTP requests, and **React-Router** for routing. **React Hooks** were used throughout the application, including both buit-in hooks like **useState** and **useEffect** as well as **custom hooks**. A custom hook was used to design reuseable form logic in accordance with **Don't Repeat Yourself (DRY)** best practices. Responsiveness is implemented using **CSS Media Queries**.

### Cloud & Devops
Each microservice was containerized usng **Docker** and deployed in an **AWS EC2** instance. The client application was containerized using Docker and deployed in **AWS Elastic Beanstalk**. OpinionMarket, therefore, leverages a cloud stack consisting of both **Infrastructure-as-a-Service (IaaS)** and **Platform-as-a-Service (PaaS)** components. All databases use **MongoDB Atlas** a cloud-native **NoSQL** database solution. An automated **CI/CD pipleline** and automated unit and integration testing were built in to the microservice's **Maven** build cycle. This was done using **Maven profiles**, **JUnit**, the **Surefire plugin**, the **Failsafe plugin**, the **Dockerfile for Maven plugin from Spotify** and **Watchtower**. The Dockerfile for Maven plugin pushes a **Docker image** to **Docker Hub** where it is detected by and deployed by Watchtower. An advatage of this solution is that it is independent of the underlying cloud service and relies solely on Docker. If any integration test or the Docker build fails, then the Maven build also fails.

### Diagrams  
#### Physical Architecture
![Phyiscal Architecture](/images/PhysicalArchitecture.png)

#### Logical Architecture
![Logical Architecture](/images/LogicalArchitecture.png)

#### UML Class Diagrams
The following UML class diagram depicts the classes in the user microservice together with their relationships and the multiplicities of those relationships.
![User Service](/images/userUML.png)

See the complete Design Specification [here](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/DesignSpecification.docx "Design Specification") for full details.

## Next 
[Risks & Challenges](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/RisksAndChallenges.md "Risks & Challenges")
