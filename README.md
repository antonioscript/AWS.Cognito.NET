# AWS.Cognito.NET
This repository demonstrates how to integrate Amazon Cognito with .NET applications. It covers user authentication and authorization workflows using AWS Cognito's User Pools and Identity Pools

# Summary

- [AWS Cognito](#aws-cognito)
  - [User pools](#user-pools)
  - [Identity pools](#identity-pools)
  - [Federated identities](#federated-identities)
  - [Multi-Factor Authentication (MFA)](#multi-factor-authentication-mfa)

- [Application](#application)
  - [Client Credentials Flow & Password Grant Flow](#client-credentials-flow--password-grant-flow)

- [Creating an Amazon Cognito User Pool](#creating-an-amazon-cognito-user-pool)
  - [Overview](#overview)
  - [Password policy](#password-policy)
  - [Multi-factor authentication](#multi-factor-authentication)
  - [User account recovery](#user-account-recovery)
  - [Self-service sign-up](#self-service-sign-up)
  - [Attribute verification and user account confirmation](#attribute-verification-and-user-account-confirmation)

- [Client Credentials Flow: Setup & Testing](#client-credentials-flow-setup--testing)
  - [Resource servers](#resource-servers)

- [References](#references)


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

</br>

![image](https://github.com/user-attachments/assets/9d8a3fa7-6204-4cf2-ae41-53b6654d332d)


----


![image](https://github.com/user-attachments/assets/4ccaebcd-de9b-497e-b1a3-5d6699c8c7af)


-----

## Overview

</br>

![image](https://github.com/user-attachments/assets/d5c3ac69-cb7e-420c-a828-9b5f1789a39b)

-----


## Password policy 

</br>

![image](https://github.com/user-attachments/assets/557c454d-1cb4-43c2-8bf2-56b216a82f74)

-----

![image](https://github.com/user-attachments/assets/2664a543-76d0-48da-a32c-a924a09b8240)


----


</br>

## Multi-factor authentication 

</br>

![image](https://github.com/user-attachments/assets/f0768eac-1cb3-4883-8c61-eb492f247a8d)

----

![image](https://github.com/user-attachments/assets/cdb1c0dd-ed55-4e79-8fd4-e0f0d78762e4)


--------

## User account recovery

</br>

![image](https://github.com/user-attachments/assets/41ce3dce-6c14-434e-a0b2-f4dfaa21495e)

-----

</br>

![image](https://github.com/user-attachments/assets/5f4d77c6-db0d-4320-86f3-c255086da8fe)


## Self-service sign-up

</br>


![image](https://github.com/user-attachments/assets/3ce48325-a1d0-4400-95d5-94045afad9c1)

----

![image](https://github.com/user-attachments/assets/967aadb9-ceae-45c8-b7ed-604aae4001e8)

---------

## Attribute verification and user account confirmation

</br>

![image](https://github.com/user-attachments/assets/eb3d5350-c067-4d48-8a5c-d63d4f9a52ac)



----

![image](https://github.com/user-attachments/assets/816f40ff-1387-42cc-99e0-b2afc51eeecc)

----


# Client Credentials Flow: Setup & Testing

## Resource servers

![image](https://github.com/user-attachments/assets/e3c82b06-dd75-44dc-9351-9a96febc606d)

---

![image](https://github.com/user-attachments/assets/b79f3eaa-e50b-4819-bbcc-af25fc103711)




# References

https://codewithmukesh.com/blog/securing-dotnet-webapi-with-amazon-cognito/
