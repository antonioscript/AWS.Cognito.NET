# AWS.Cognito.NET
This repository demonstrates how to integrate Amazon Cognito with .NET applications. It covers user authentication and authorization workflows using AWS Cognito's User Pools and Identity Pools

# AWS Cognito
Key features of Amazon Cognito include:

- **User pools**: A user directory that helps manage sign-ups, sign-ins, and user profiles.
- **Identity pools**: Enable users to authenticate and access AWS resources securely.
- **Federated identities**: Allow users to log in with their existing credentials from third-party identity providers.
- **Multi-Factor Authentication (MFA)**: Enhance security by requiring multiple verification steps for users.

# Application
_Firstly, we will go through setting up the client credentials and password flow in Cognito. Next, we will test if these flows are able to generate Tokens for us. Once the token generation is sorted, we will build an ASP.NET Core Web API which will be secured by Amazon Cognito and verify that the API is able to take in both of the tokens (from each flow) and is able to authenticate requests into a secure API endpoint._

## Client Credentials Flow & Password Grant Flow
- As mentioned earlier, we will look into the Client Credentials flow, where the client (our web API) will pass its client id and the secret to Cognito in exchange for an access token. Here, user consent won’t be required. This mode of authentication is typically used for server-to-server communication and when the client owns the protected resource.

- On the other hand, the password flow is used when the user needs to authenticate into a server to access resources. Here, the user would send his credentials like username and password.
We will implement both of these approaches

# Creating an Amazon Cognito User Pool


# References

https://codewithmukesh.com/blog/securing-dotnet-webapi-with-amazon-cognito/
