# santander Dev Week 2023
Java RESTful API created for Santander Dev Week

# Main Technologies

- **Java 17**: We will utilize the latest LTS version of Java to leverage the most recent innovations offered by this robust and widely adopted language.
- **Spring Boot 3**: We will be working with the latest Spring Boot version, which enhances developer productivity through its powerful auto-configuration capabilities.
- **Spring Data JPA**: We will delve into how this tool can streamline our data access layer, simplifying integration with SQL databases.
- **OpenAPI (Swagger)**: We will create effective and comprehensible API documentation using OpenAPI (Swagger), seamlessly aligned with the high productivity that Spring Boot provides.
- **Railway**: Railway facilitates cloud deployment and monitoring of our solutions, offering various databases as services and CI/CD pipelines.

## Class Diagram

``` mermaid
classDiagram
    class User {
        - name: String
        - account: Account
        - features: Feature[]
        - card: Card
        - news: News[]
    }
    
    class Account {
        - number: String
        - agency: String
        - balance: Number
        - limit: Number
    }
    
    class Feature {
        - icon: String
        - description: String
    }
    
    class Card {
        - number: String
        - limit: Number
    }
    
    class News {
        - icon: String
        - description: String
    }
    
    User "1" *-- "1" Account
    User "1" *-- "N" Feature
    User "1" *-- "1" Card
    User "1" *-- "N" News
```
