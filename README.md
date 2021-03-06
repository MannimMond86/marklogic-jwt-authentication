#Securing a REST API using JWT and MarkLogic

> Please note that the project requires you to have Node.js v4.4.5 or above and MarkLogic v8.0 or above.

##Setup project
Before setting up the project please make sure that the details in `settings.js` match the settings of your environment, if not, please update as necessary:

```javascript
const username = 'admin';
const password = 'admin';
const host = 'localhost';
const port = 8000;
```

> Please note that an out-of-box MarkLogic installation will have a REST API instance running on port 8000.
g
The first step would be to install the project dependencies by executing `npm i`.

To insert the initial dataset to the database you can execute `npm run setup`.

> To delete all the documents that have been inserted via the installation please run `npm run delete`.

##Token creation
To create a token please run `npm run createToken`.

##Start the application
To start the application itself please run `npm start`.

> Development mode is enabled if you start the application using `npm run startDev`. Development mode uses `nodemon` to start the application.

##Accessing the secured endpoint
The easist way to access the secured endpoint is to use the following curl statement: `curl -H 'Authorization: Bearer [access_token]' http://localhost:8080/api/characters` where `[access_token]` is the token created using the previous step.

##Further information
For further information please visit: [http://developer.marklogic.com/blog/securing-a-rest-api](http://developer.marklogic.com/blog/securing-a-rest-api)
