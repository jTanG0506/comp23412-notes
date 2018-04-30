# Week 4: Security

**Security** is fundamentally about protecting assets, which may be tangible items, such as a web page or a database, or they may be less tangible items, such as company reputation.

### Definitions
- A **threat** is any potential occurence, malicious or otherwise, that could harm an asset
- A **vulnerability** is a weakness that makes a threat possible
- An **attack** is an action that exploits a vulnerability or enacts a threat

### Web application security vulnerabilities
- **Code injection** is when malicious executable code is insert into legitimate traffic sent to an endpoint
- **Poor authentication and session management** could compromise user identities in a variety of different ways
- **Cross-site scripting** is similar to code injection, but involving scripts instead

## Authentication
**Authentication** is the process of recognizing a user's identity. It is the mechanism of associating an incoming request with a set of identifying credentials.

We compare the credentials provided with those stored in the authorized user's information database, either on a local operating system or within a authentication server. Authentication is the first process that is done, before permission and throttling checks occur.

Credentials usually take the form of a password, which is a secret and known only to the invididual and the system. Other methods of authentication include RFID cards, PIN numbers, biometrics, USB tokens, one-time password tokens and two-factor authentication.

## Authorization
Authorization is a security mechanism to determine access levels or privileges related to system resources, including files, services, computer programs, data and application features. This is the process of granting and denying access to a network resource which allows the user to access to various resources based on the user's identity.

For example, admins of a website should be able to access everything, the support team may be able access user details and guests may have very limited access (as they generally don't need authentication).