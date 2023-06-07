## What is OAuth

1. What is OAuth?
-It's an open-standard authorization protocol or framework that allows unrelated servers and services to safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential. It is essentially a method that allows one website to access another website's resources on behalf of a user, which means users don't have to share password data with every website or app. OAuth was created and strongly supported by Twitter, Google, and other companies, and became an open standard in 2010.

2. Give an example of what using OAuth would look like.
An example of using OAuth is when you log onto a website and it offers one or more opportunities to log in using another website’s/service’s credentials. You then click on the button linked to the other website, the other website authenticates you, and the original website logs you on using permission gained from the second website. Another example is attaching files stored in cloud storage (like Google Drive) to an email in Gmail. OAuth would be used behind the scenes to authenticate and access the protected files without requiring a second login.

3. How does OAuth work? What are the steps that it takes to authenticate the userThe user has already signed into one website or service.

- The user then initiates a feature/transaction that needs to access another unrelated site or service.
- The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.
- The second site generates a one-time token and a one-time secret unique to the transaction and parties involved.
- The first site gives this token and secret to the initiating user’s client software.
- The client’s software presents the request token and secret to their authorization provider.
- If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the second website.
- The user approves a particular transaction type at the first website.
- The user is given an approved access token.
- The user gives the approved access token to the first website.
- The first website gives the access token to the second website as proof of authentication on behalf of the user.
- The second website lets the first website access their site on behalf of the user.
- The user sees a successfully completed transaction occurring.

4. What is OpenID?
OpenID is an open standard and decentralized authentication protocol that allows users to be authenticated by co-operating sites (known as relying parties) using a third-party service. It allows the user to be authenticated by sites using a third-party service, eliminating the need for webmasters to provide their own ad hoc login systems, and allowing users to log into multiple unrelated websites without having to have a separate identity and password for each. OpenID is for authentication (proving who you are), whereas OAuth is for authorization (to grant access to functionality/data/etc.. without having to deal with the original authentication).


## Authorization and Authentication flows

1. What is the difference between authorization and authentication?
Authentication is the process of verifying the identity of a user, device, or system. It commonly involves validating whether a user's credentials, such as a username and password, are valid. In short, it answers the question, "Are you who you say you are?"
Authorization, on the other hand, is the process of granting or denying access to specific resources once a user's identity has been authenticated. It answers the question, "What are you allowed to do?"

2. What is Authorization Code Flow?
 This is a common pattern in OAuth 2.0 that is used by applications to obtain an access token. It is intended for applications that can securely maintain a client secret between themselves and the authorization server. In this flow, the user's credentials are never exposed to the application. Instead, the application directs the user to an authorization server, which then redirects back to the application with an authorization code. This code is exchanged for an access token.

3. What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?
 This is an enhanced version of the Authorization Code Flow that prevents an attacker from intercepting the authorization code and using it to obtain an access token. In this flow, the client (typically a public client, such as a native or single-page application) creates a code verifier and its transformed value called code challenge. The client sends the code challenge and a method to the authorization server. The server associates the challenge and method with the authorization code that it sends back to the client. When the client sends this authorization code to the token endpoint to exchange it for tokens, it also includes the original code verifier. The server transforms this and compares it to the previously associated code challenge to ensure they match.

4. What is Implicit Flow with Form Post?
This flow is intended for applications that can't securely maintain a client secret between themselves and the authorization server, such as single-page apps (SPAs). The application redirects the user to the authorization server, which in turn redirects back to the application with an ID token and access token (if requested). The tokens are returned as form post parameters and are intended for user authentication. The implicit flow with form post has been largely superseded by the Authorization Code Flow with PKCE for most scenarios.

5. What is Client Credentials Flow?
This flow is used for machine-to-machine communication, where a client needs to directly access resources from the server, and there is no user involved. The client sends a request with its client ID and client secret and receives an access token in response.

6. What is Device Authorization Flow?
This flow is used for devices that don't have an easy way for a user to input information (e.g., smart TVs, IoT devices). The device displays a URL and a device code. The user navigates to the URL on a separate device and inputs the device code. After that, the user logs in and approves the device. Once approved, the device can request tokens.

7. What is Resource Owner Password Flow?
This flow allows the client to send the resource owner's (user's) username and password directly to the authorization server to obtain an access token. It's only recommended for scenarios where the client is highly trusted, and other more secure flows can't be used. This flow is considered risky and is generally discouraged due to the need to directly handle and store user credentials.