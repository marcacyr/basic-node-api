# basic-node-api
This is a barebones API built using NodeJS and Express. Feel free to make use of this as a basis for a project.

***The API uses JWT tokens in the authentication.***

***The API relies on Mongoose, and by extension on MongoDB as the database.***

## Setup
1. Clone this repo to your local machine.
2. Run ```npm install bcrypt-nodejs body-parser express jsonwebtoken mongoose morgan --save```

This will install all dependencies and anything else needed based on package.json. You could also just run ```npm install``` and let npm do the work. I just tend to be explicit. It's your call whatever works best for you.

## Usage
To use this as a basis for an API, you will have to create a file called config.js at the root level.

In that file, you will have to set an export so that your server.js file can make use of you config settings. The config file
should be structured as follows:

```
module.exports = {
  'port': process.env.PORT || 8888,
  'database': 'path_to_your_db_of_choice',
  'secret': 'your_secret_string'
}
```

Note: The "database of choice" for your app must be a MongoDB database unless you change out the packages to use something created
for a different type of DB. You can conceivably use anything. It is simply that this API is set up to work with MongoDB out of the
box. Also note that the ***server.js file already requires config.js by default*** so you will not have to add a require line, but you absolutely need this file to run this server without error.
