# https://coderrocketfuel.com/article/create-and-deploy-an-express-rest-api-to-a-digitalocean-server#create-a-node-js-and-express-rest-api

mkdir app
cd app
npm init

# give the data project then

# install Express

npm install express --save

touch index.js

# paste this to index.js file

const express = require("express")

const PORT = process.env.PORT || 5000
const app = express()

app.get("/", (req, res) => {
res.send("Welcome to your App!")
})

app.listen(PORT, function () {
console.log(`Express server listening on port ${PORT}`)
})

# then modify the package.json file -- add the following on "scripts"

"start":"home index.js"

# to run the code use

npm start

http://localhost:5000/

# this returns Welcome to your app

# just a test ---

For testing purposes, try any different URL. For example:
http://localhost:5000/users
You should see a "Cannot GET /users" message.

## That message is shown because we haven't configured that route yet. In the next step, we'll get additional routes like that configured.

# To get testing data to work with, use the free Json Placeholder

---

# To retrieve the data from Json Placeholder, we'll use the Axios npm package.

npm install axios --save

---

# Add a GET Request
