# Choosing Identity Provider

* Status: proposed
* Date: 2023-08-15

Technical Story: Choosing Identity Provider

## Context and Problem Statement

We need a new Identity Providers which is secure and supports Wuerth authtication (Ex: eShop, Orsyonline)

## Decision Drivers

* Support Wuerth Authentication (eShop, Orsyonline etc)
* Low Cost
* Deployment on Wurth IT as the this service contains User credential Data and information about clients (APIs, WebApps)
* Communication to other services (REST, Events)

## Considered Options

* Custom Implementation
* Open Source Self Managed
* Third Party Solution

## Decision Outcome

Chosen option: "Open Source Self Managed", because it allows better time to market and allows some degree of customization.

### Positive Consequences

* High time to market
* Allows apps to be integrated already.

### Negative Consequences

* Some very specific customisation might not be supported.

## Pros and Cons of the Options

### Custom Implementation

Wrtitng the Identity provider code from scratch.

* Good, because Have greater control and customisation.
* Good, because Can choose the programming Language
* Good, because No costs
* Bad, because High time to market.
* Bad, because Need to maintain the code.
* Bad, because Be aware of security vulnerabilities.

### Open Source Self Managed

Using an OpenSource solution like Keycloak, WSo2 etc.

* Good, because Out of box Identity provider Implementation.
* Good, because Supports ODIC & OAuth
* Good, because No costs
* Bad, because Can be limiting in terms of customization.
* Bad, because Should check if Wuerth Authentication is supported.
* Bad, because Programming Language is dependent on solution.
* Bad, because Need Keep the base updated and work around breaking changes.

### Third Party Solution

Complete implementaion of IDP managed by Third Party Service

* Good, because Out of box Identity provider Implementation.
* Good, because Supports ODIC & OAuth
* Bad, because Low or minimum customisation.
* Bad, because Might not support Wuerth Authentication which does not follow ODIC standard.
* Bad, because Conneting to other services might not be possible.
* Bad, because Data is stored at Third party solution except on-premise solution
* Bad, because Costs based on MAU (Monthly Active Users)
