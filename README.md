# Ethos Integration Postman Examples

Postman is an API Development Environment that allows for the development and testing of APIs, like those in Ethos Integration. Postman is a free and cross-platform application.  Get Postman here -> https://www.getpostman.com

This repository contains a Postman *collection* and *environment*. A *collection* is simply a group of related API requests. The collection here contains examples of how to do things in Ethos Integration like obtaining an access token, calling GET/POST/PUT/DEL on a resource and consuming change-requests. An *environment* is a set of key-value pairs, essentially variables, that can be shared among API requests. The environment in this repository is used to store an API key and JWT access token.

For more Postman learning and documentation start here -> https://learning.getpostman.com/concepts/

## Getting Started

Clone or download the repository to your machine. The collection and environment files are in json format. Launch Postman and import the collection and environment json file by clicking the **Import** button at the top of the Postman application.

![](/screenshots/postmanImport.png)

Add your API key to the Environment Variable 'ethosApiKey'.  Update the 'ethosIntegrationUrl' if needed for your region.

![](/screenshots/postmanVarSetup.png)


Finish the setup by selecting the environment from the dropdown menu so that Postman will use it.

![](/screenshots/postmanSelectEnvironment.png)

You are now ready to execute an HTTP request.  For example, click Collections >> Ethos Integration Examples >> Some Basics >> Read all courses resource and then hit Send.  Notice the results show below.

![](/screenshots/postmanRunRequest.png)


## Pre-request Script
 This collection contains a pre-request script to simplify calling ethos end points.  The script will automatically:
 1. Prepend the ethos integration url to any request that needs it.  For example, to call https://integrate.elluciancloud.com/persons end point - you only need to enter 'persons'.  Any endpoint that does not have the /api/{resource} pattern you will need to enter the full url.
 2. Manage Authorization token.  The script will get, store and use the authorization token. This requires a valid value in the variable 'ethosApiKey'
 3. Encode query string parameters.




This document was written using Postman March 2023 (v10.12)
