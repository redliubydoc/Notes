# What are authentication and authorization?

    In simple terms, authentication is the process of verifying who a user is, while authorization is the process of verifying what they have access to.

    Comparing these processes to a real-world example, when you go through security in an airport, you show your ID to authenticate your identity. Then, when you arrive at the gate, you present your boarding pass to the flight attendant, so they can authorize you to board your flight and allow access to the plane.

    In short, access to a resource is protected by both authentication and authorization. If you can't prove your identity, you won't be allowed into a resource. And even if you can prove your identity, if you are not authorized for that resource, you will still be denied access.

    https://auth0.com/docs/get-started/identity-fundamentals/authentication-and-authorization


| Authentication | Authorization |
| :-------------:|:-------------:|
| Determines whether users are who they claim to be | Determines what users can and cannot access |
| Challenges the user to validate credentials | Verifies whether access is allowed through policies and rules |
| Usually done before authorization | Usually done after successful authentication |
| Generally, transmits info through an ID Token | Generally, transmits info through an Access Token |
| Generally governed by the OpenID Connect (OIDC) protocol | Generally governed by the OAuth 2.0 framework |
| Example: Employees in a company are required to authenticate through the network before accessing their company email | Example: After an employee successfully authenticates, the system determines what information the employees are allowed to access |




# What is OAuth2?

    OAuth 2.0, which stands for “Open Authorization”, is a standard designed to allow a website or application to access resources hosted by other web apps on behalf of a user. It replaced OAuth 1.0 in 2012 and is now the de facto industry standard for online authorization. OAuth 2.0 provides consented access and restricts actions of what the client app can perform on resources on behalf of the user, without ever sharing the user's credentials.

    Although the web is the main platform for OAuth 2, the specification also describes how to handle this kind of delegated access to other client types



# OAuth2.0 Roles

    The idea of roles is part of the core specification of the OAuth2.0 authorization framework. These define the essential components of an OAuth 2.0 system, and are as follows:

    Resource Owner: The user or system that owns the protected resources and can grant access to them.

    Client: The client is the system that requires access to the protected resources. To access resources, the Client must hold the appropriate Access Token.

    Authorization Server: This server receives requests from the Client for Access Tokens and issues them upon successful authentication and consent by the Resource Owner. The authorization server exposes two endpoints: the Authorization endpoint, which handles the interactive authentication and consent of the user, and the Token endpoint, which is involved in a machine to machine interaction.

    Resource Server: A server that protects the user’s resources and receives access requests from the Client. It accepts and validates an Access Token from the Client and returns the appropriate resources to it.





Grant Types

    1. Authorization Code
    2. Client Credentials
    3. Refresh Token
    4. Implicit (deprecated)
    5. Password or Resource Owner Credentials (deprecated)