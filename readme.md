## Advanced Express
https://www.linkedin.com/learning/advanced-express

Similar express app than repository 'Building_Website_NodeJS_Express' using pug template engine (server/views) instead of ejs.

## CH00 - Prereq

eslint plugin installed
npm install
npx mocha test/server/app.test.js
npm start

Connection to mongodb

- As soon as the database connection is set up using https://cloud.mongodb.com/ > cluster > creates 3 databases development, production and test

# setup Cloud server database using MongoDB

https://cloud.mongodb.com/
Using gmail account (rlptc)
Create a free cluster available for < 500MB: nodedeploy
server created = mongodb+srv://learning:learning@nodedeploy-ehxpw.mongodb.net

Using cloud.mongodb.com browser:

- Click on Cluster 'nodedeploy' url
- Go to Collections tab
- Create 3 databases :
  . AdvExpressTest (enter default collection: users)
  . AdvExpressProduction (enter default collection: users)
  . AdvExpressDevelopment (enter default collection: users)
- collection users
- go to security > network access > whitelist > id my ip adress
- go to security > database access > user > check or create new user with read+write any database access
- go to cluster 'nodedeploy' > connect > choose connection method
  mongodb+srv://learning:<password>@nodedeploy-ehxpw.mongodb.net/<dbname>?retryWrites=true&w=majority
  mongodb+srv://learning:learning@nodedeploy-ehxpw.mongodb.net/AdvExpressTest?retryWrites=true&w=majority
  mongodb+srv://learning:learning@nodedeploy-ehxpw.mongodb.net/AdvExpressProduction?retryWrites=true&w=majority
  mongodb+srv://learning:learning@nodedeploy-ehxpw.mongodb.net/AdvExpressDevelopment?retryWrites=true&w=majority

From new cluster created in https://cloud.mongodb.com/, check Connect page: it is possible to connect using

- MongoDB Shell (linux)
- Application Driver like Node.js
- Compass
  Using MongoDB Compass :
- connect using connection SRV: mongodb+srv://learning:learning@nodedeploy-ehxpw.mongodb.net
- create database: database name + collection name
- then using compass, display the nodejsdeploy database: take note of the url displayed at header:

nodedeploy-ehxpw.mongodb.net/AdvExpressDevelopment
This is used by application URI.

## setup env

- Edit end rename .env
- Make sure to never commit .env to a version control system
- (see also .gitignore)

open vscode in Ex_Files_Advanced_Express/CH04-meetup
eslint plugin installed
npm install
If issue with some component, update them with latest: such as
- npm install --save bcrypt@latest
- npm install sharp@latest
npx mocha .\test\db\connect.js
npx mocha test/server/app.test.js
npm start

CH01-Building Blocks and inernals of Express
- Exploring Express components and APIs
- Important Express Middleware
- Create a template engine for express
CH02-Use mongoDB and MOngoose to manager users
- Setting up a hosted MongoDB server
- Connecting to MongoDB
- Adding MOngoDB and Mongoose to an Express project
- Creating a user schema for mongoose
- Using bcrypt to hash and validate passwords
- Adding password encryption and validation to a Mongoose model
- Creating a user registration route
- Testing the form and reviewing the data in MongoDB
CH03-Authenticate and Authorize Users
- Understanding cookies and sessions
- Adding cookies and sessions to Express
- Inspecting the session object
- Introduction to Passport
- Adding Passport to Express
- Setting up an authentication strategy for Passport
- Serializing and deserializing users
- Creating a login form with Passport
- Providing a logout link
- Authentication vs. authorization
- Protecting routes
CH04-Handle File Uploads and Process Images
- File upload basics
- Handling multipart form data with multer
- Resizing and storing images with sharp
- Creating an image handling middleware
- Serving images
CH05-Deployment and Running in Production
- Tuning Express performance: NODE_ENV and compression
- Tuning Express performance: Further measures
- Add logging
- Using the Node.js cluster module
- Securing an Express application
- Deployment and operation with PM2
- Running behind a web server



