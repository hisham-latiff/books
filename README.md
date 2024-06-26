<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->




<!-- PROJECT LOGO -->
<br />
<div align="center">
 
<h3 align="center">GraphQL Spring Boot Demo Application</h3>

</div>





<!-- ABOUT THE PROJECT -->
## About The Project

[//]: # ([![Product Name Screen Shot][product-screenshot]]&#40;https://example.com&#41;)

This Project Demostrate Basic GraphQL Implementation in Spring Boot using on-memory data in form of list.
The data example use in this project illustrate the data of books.





### Built With

This section should list any major frameworks/libraries used to bootstrap your project. Leave any add-ons/plugins for the acknowledgements section. Here are a few examples.

* Maven
* Java





<!-- GETTING STARTED -->
## Getting Started



### Prerequisites

This project require Java Development Kit.
* Java JDK 17
  

### Installation

_Below is the installation instruction for this project._

[//]: # (1. Get a free API Key at [https://example.com]&#40;https://example.com&#41;)
1. Clone the repo
   ```sh
   git clone git@github.com:hisham-latiff/books.git
   ```
2. Install JDK and JRE
   - Installer file can be found at Java Website
   - Update Environment for JAVA_HOME
   ```sh
    %JAVA_HOME% = <jdk-directory> 
   ```
   

3. Build and run with `maven`. Make sure you are in project root directory.
   ```cmd
    mvnw spring-boot:run
   ```




## Querying GraphQL

_Below is the querying instruction for this project._

[//]: # (1. Get a free API Key at [https://example.com]&#40;https://example.com&#41;)
1. Open browser and go to      <a href="http://localhost:8181/graphiql">https://localhost:8181/graphiql</a>

2. Before Running Make sure <a href="https://github.com/hisham-latiff/GraphQL-in-Spring-Boot-Demo/blob/4d10287b5a03ac65b1ed7c89a936372f842a0cea/src/main/resources/application.properties">application.properties</a> file contains:-
   ```sh
    spring.graphql.graphiql.enabled=true
   ```
3. Querying GraphQL.
    
   ```sh
    query {
       allBooks{
          title
          pages
          rating {
              star
          }  
          author {
              firstName
              lastName
          }  
       }
    }  
   ```


3. Upon query success, graphql will return the data requested in json object structure as below.
   ```json
      {
        "data": {
            "allBooks": [
            {
                "title": "Reactive Spring",
                "pages": 484,
                "rating": {
                    "star": "⭐️⭐️⭐️⭐️⭐️️️️"
                },
                "author": {
                    "firstName": "Josh",
                    "lastName": "Long"
                }
            }, ...
            ]
        }
      }

   ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>













