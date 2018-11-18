#  System Architecture

The overall architecture of the software for Elections Commission follows a microservices architecture. The conceptual architecture is shown below.

<p align="center">
  <img src="overallarch.png">
</p>

**Web UI** & **Mobile UI** - Web and mobile applications are used by various parties to access different features of the overall system. Each app will be applicable to particular classes of users and the availability, features and functionality will be controlled based on the user.

**3rd Party API Consumers** - These are other systems that connect to various APIs offered by Elections Systems for system to system integration. This can be for result acquisition, for complaint tracking and so on.

**Web Server** - The Web servers are the starting point for all users who access via Web UIs. Some of these will only be available internally within the Elections Commission VPN while others will be available externally.

**Identity Manager** - The Identity Manager is responsible for authenticating all users and for providing high level authorization information for particular applicaitions. Fine-grained authorization will be the responsibility of particular services.

**API GW** - The API Gateway is the entrypoint for all external accesses to the services that comprise the functionality of all elections systems. The API Gateway uses the Identity Manager for authentication and authorization prior to forwarding requests to the services.

**Service** - The services are what implement the various features and functions of the overall system. Note that some of these may be of the <a href="https://samnewman.io/patterns/architectural/bff/">Backend for Frontend</a> nature and we may choose to use an integration layer specifically for such services.

**Storage** - This layer contains all the various storage systems we will use for different kinds of services. Some of the databases may be directly associated with one services (in a true microservice fashion) while others may be shared. 

**Event Bus** - The event bus will be used for certain microservice to microservice communications as well to publish information generally across different systems.

Specific aspects of the architecture are discussed in the following documents:

* <a href="security.md">Security Architecture</a>