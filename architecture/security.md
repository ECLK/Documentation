# Security Architecture

Security considerations for Elections System involve the following aspects:

* Access control via authentication and authorization to ensure only appropriate users are allowed to access the parts of the system they are authorized to.
* Data privacy for both data at rest and while being transferred to ensure no unauthorized or abusive actions are possible.
* Deployment security to ensure the integrity of the entire solution.

## User Management

Every application and API access will require authentication and  authorization. Credentials and permissions will be granted based on the kind of user accessing and role(s).

Users are managed by the identity manager component with different user stores for the different kinds of users and by federating to external user management systems. 

The currently planned different kinds of users are the following:

* EC Staff - These users are regular (full time, part time, consulting) staff of the EC and will be coming from the internal LDAP user store.

* Election Staff - These users are those who are provisioned during the execution of a particular election. They will be given appropriate permissions that are valid only during that period and they will have no access after the election is over. These users will be kept in a separate OU (organization unit) within the same internal LDAP server.

* Citizens - These are citizens who are allowed to login and update their data. The expectation is to federate this login from the Grama Niladari system that is currently under development.

* E2G Users - These are various government organizations that require access to various EC systems either via the applications or via the API. These include Police.

* Media - These are registered (?) media organizations that have been given API access to various APIs. These will be in another OU in the same LDAP.

* Visitors - These are random people from the Internet who visit the website and for whom we need some kind of authentication in order for them to perform transactions (such as reporting a violation).

### Architecture

<p align="center">
  <img src="umarch.png">
</p>

### LDAP Design

(Details on the LDAP OU structure and other details)

### Federation for Citizens

The eGrama Niladari project will be creating a digital identity (a username & password combination) for all citizens. 

## Link Security
