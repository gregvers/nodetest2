# nodetest2
Creating a Simple RESTful Web App with Node.js, Express, and MongoDB
from
https://closebrace.com/tutorials/2017-03-02/creating-a-simple-restful-web-app-with-nodejs-express-and-mongodb

# cd db
# docker build -t nodetest2db .
# docker run -it --name myMongoDB -p 27017:27017 nodetest2db
// docker run -d --name myMongoDB -p 27017:27017 nodetest2db
To get a client to Mongo DB
# docker exec -it myMongoDB mongo
To insert a user:
db.userlist.insert({'username' : 'test1','email' : 'test1@test.com','fullname' : 'Bob Smith','age' : 27,'location' : 'San Francisco','gender' : 'Male'})

# cd app
# docker build -t nodetest2 .
# docker run -it -p 3000:3000 --link myMongoDB:nodetest2db nodetest2 bash
Run:
# npm start
