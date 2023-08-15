# Choosing Authorization Server

* Status: proposed
* Date: 2023-08-15

Technical Story: Authentication and Authorization

## Context and Problem Statement

We need to control the access to resources by clients. Hence we need an Authorization server which checks or informs the resource server to allow or block the access to resource based on client and user.

## Decision Drivers

* Fast resolution of access

## Considered Options

* Scopes in the JWT
* Custom Authorization Server

## Decision Outcome

Chosen option: "", because comes out best.

## Pros and Cons of the Options

### Scopes in the JWT

Scopes can be added to JWT and the resource server can decode the token to check for authority.

* Good, because No need to check with another service for authority.
* Bad, because Scopes in JWT increases the size of Token.
* Bad, because Scopes need to be defined at Authentication Server
* Bad, because Change in scopes can take time to affect.
* Bad, because Complex access scenarios need multiple scopes.
* Bad, because As of now unclear on per company based access

### Custom Authorization Server

Scopes and access is checked with a third party.

* Good, because JWT size is small and hence smaller request size.
* Good, because Complex scope can be realized.
* Bad, because Service need to request the Authorization Server. Latency can be minimised by Cache
