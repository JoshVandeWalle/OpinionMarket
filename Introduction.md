# Introduction  

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


### Business Problem and Solution  
The moniker OpinionMarket captures the concept of a marketplace of ideas making it the perfect name for an application all about sharing information and thoughts. The application is a web platform for social news and community-driven discussion that facilitates discourse between individuals based on common interests. OpinionMarket allows users to join communities of their choice, post content in those communities, comment on content posted by others, upvote or downvote any post or comment, and send direct messages. These features support the creation of a vast ecosystem of meaningful discussions.
  
The platform is designed to be easy for anyone to use and helpful for everyone. Whatever a user is interested in, be it a hobby, professional skill, or theoretical physics, they can find or start an online community dedicated to it. Community rules establish user-enforced behavioral regulations that keep communities focused on their topic. Customization features make communities unique, give them character, and allow them to stand out. The wealth of features they provide make OpinionMarket communities an excellent place to look for help, show off accomplishments, or find discussion of just about anything. The application presents an intuitive and friendly user interface that makes it easy to dive-in and start browsing content-rich communities.  

### Technical Problem and Solution  
OpinionMarket is designed using a microservice architecture based on REST APIs. This architecture solves business problems but creates technical problems. Microservice architecture divides an application into smaller applications to increase the maintainability, technical flexibility, scalability, and fault-tolerance of the overall system. Changes made to one microservice do not force the entire application to be re-compiled, meaning the code is easier to maintain. Maintainability also benefits from microservices being more simple, from a code standpoint, than monolith applications. This makes a microservice easier for a developer to understand when designing and building an update. Microservices can use different frameworks and databases based on what technology provides the best solution for the problem they are solving. This technical flexibility means development teams are no longer forced to use technologies unsuitable to the task they are working on. Microservices make scaling up an application easier. Since services are separate, it’s easier to scale only the services that must be scaled, improving efficiency. If there is a problem in one microservice the rest of the system is far less likely to be affected than with a monolith architecture because of the code boundaries between microservices. There is, however, a trade-off involved when leveraging microservices. Because the database-per-service pattern is used in the architecture, maintaining data consistency is a challenge. Another challenge is that service calls require service orchestration and discovery to be in place.

OpinionMarket solves these common microservices problems. Service orchestration and data consistency are handled using sagas and compensation transactions. The API gateway orchestrates sagas and, if necessary, performs compensation transactions. All API calls depend on service discovery for routing. This is handled by the Discovery Service which is built using the Spring Cloud Eureka tool.
See the complete Design Specification [here.](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/DesignSpecification.docx "Design Specification") 


### Who Made OpinionMarket? ###  
My name is Josh Van de Walle. I am a software engineer with a passion for solving problems in the most efficient way possible. 
- See my [LinkedIn profile](https://www.linkedin.com/in/joshv42/ "LinkedIn")  
- Download my [resume](https://drive.google.com/file/d/14kEgO7PI51CU9ZVqGy6FagDcKbD2Rhc_/view?usp=sharing "Resume")
## Next 
[Requirements](https://github.com/JoshVandeWalle/OpinionMarket/blob/main/Requirements.md#requirements "Requirements")
