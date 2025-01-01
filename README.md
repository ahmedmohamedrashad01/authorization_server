# Authorization Server with Spring Boot and Spring Authorization Server  

This project is a robust **Authorization Server** built using **Spring Boot** and **Spring Authorization Server**. It supports secure authentication and authorization mechanisms, including **Client Credentials Grant Type**, token customization, and scope management.  

## Features  

### 🔐 Authentication  
- **Client Authentication**: Supports `CLIENT_SECRET_BASIC` for secure client identification.  

### 🛂 Authorization  
- **Grant Types**: Implements the `CLIENT_CREDENTIALS` grant type, enabling machine-to-machine communication.  
- **Scopes Management**: Configured scopes like `OPENID`, `ADMIN`, and `USER` to ensure precise permission control.  

### 🔑 Token Customization  
- **Access Token**:  
  - **Format**: Self-contained JWT tokens (`OAuth2TokenFormat.SELF_CONTAINED`).  
  - **Validity**: Access token lifetime is set to 10 minutes (`Duration.ofMinutes(10)`).  
- **Token Settings**: Easily configurable to match specific application requirements.  

### 🌐 Integration  
- Fully compatible with a **Resource Server**, enabling secure access to protected resources.  

## Tech Stack  
- **Java 21+**  
- **Spring Boot 3.3.5**  
- **Spring Authorization Server 1.4.1**  
- **OAuth2 & OpenID Connect**  

## Getting Started  

### Prerequisites  
- A compatible Resource Server for integration.  

### Setup  
1. Clone the repository:  
   ```bash
   git clone https://github.com/ahmedmohamedrashad01/authorization_server.git
   cd authorization-server
   
curl --location --request POST 'http://localhost:9000/oauth2/token' \
--header 'Authorization: Basic Base64(client_id:client_secret)' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'grant_type=client_credentials' \
--data-urlencode 'scope=ADMIN'

