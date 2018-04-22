# Introduction

As our product is mainly web based, we choose the <b>Client-server<b> architecture.
We will seperate each of our components into self contained services because:

* It's easier to modify and update each service, without other breaking.
* Services can be moved to cloud to allow:
  * Wider access range (not just from inside the home)
  * Easier service management
  * Cost reduction by only turning on services they are0 needed

## Overview

We will be basing our system on microservice architecture, we will have 4 servers running:

* Database server
* Email server
* Authentication server.
* UserInterface server

### Email server

The purpose of this service is to:

* receive incoming emails and store in the database.
* send out outgoing mail.

### Database server

Service that handles all data storage, insertions, modifications, and removal. It can only be accessed internally from the email server (with restrictions) or from the authentication server (full access).

### Authentication server

The main purpose is to validate user before database access, this way users can only modify data they have access to. Uses JWT token for authentication (allows stateless authentication).

### UserInterface server

Serve the content that will be displayed for the user. Also manages all user interactions by communicating with the Authentication server to acquire and modify data

![Alt Text](./images/sytem_context_diagram.png "Context diagram")
