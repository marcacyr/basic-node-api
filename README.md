# basic-node-api
This is a barebones API built using NodeJS and Express. Feel free to make use of this as a basis for a project.

***The API uses JWT tokens in the authentication.***

***The API relies on Mongoose, and by extension on MongoDB as the database.***

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
box.
