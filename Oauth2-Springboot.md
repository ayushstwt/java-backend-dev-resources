# OAuth2.0 Authentication with Spring Security

## Overview
This project demonstrates how to implement OAuth2.0 authentication in a Spring Boot application using Spring Security. It provides secure authentication mechanisms with various OAuth2 providers such as Google, GitHub, and more.

## Features
- OAuth2.0 authentication with external providers
- Secure API endpoints with access tokens
- User authentication and authorization
- Integration with Google and GitHub login
- Token-based security using JWT

## Technologies Used
- Java 17+
- Spring Boot 3.x
- Spring Security
- OAuth2.0
- JWT (JSON Web Token)
- Maven

## Setup and Configuration

### Prerequisites
- Java 17 or later
- Maven
- OAuth2 provider credentials (Google, GitHub, etc.)

### Clone the Repository
```sh
git clone https://github.com/your-repo/oauth2-spring-security.git
cd oauth2-spring-security
```

### Configure OAuth2.0 Providers
Modify `application.yml` or `application.properties` to include OAuth2 provider credentials.

#### Example Configuration (application.yml)
```yaml
spring:
  security:
    oauth2:
      client:
        registration:
          google:
            client-id: YOUR_GOOGLE_CLIENT_ID
            client-secret: YOUR_GOOGLE_CLIENT_SECRET
            scope: profile, email
          github:
            client-id: YOUR_GITHUB_CLIENT_ID
            client-secret: YOUR_GITHUB_CLIENT_SECRET
            scope: read:user, user:email
```

### Running the Application
```sh
mvn spring-boot:run
```

## API Endpoints
| Method | Endpoint       | Description                         |
|--------|---------------|-------------------------------------|
| GET    | `/user`       | Fetches the authenticated user     |
| GET    | `/logout`     | Logs out the authenticated user    |

## Testing OAuth2 Login
1. Start the application.
2. Navigate to `http://localhost:8080/oauth2/authorization/google` or `http://localhost:8080/oauth2/authorization/github`.
3. Authenticate with the selected provider.
4. Access secured endpoints using the obtained token.

## License
This project is open-source and available under the MIT License.

## Contact
For any queries, feel free to reach out:
- LinkedIn: [Your Profile](https://linkedin.com/in/your-profile)
- Email: your-email@example.com
