## About the project
This the backend API for a Restaurant food ordering platform. This a [NodeJS]() project built with: [ExpressJS](), [Mongoose](), [Bcrypt](), [JSONwebtoken](), [Dotenv](), [Body-Parser](), and [Nodemon]() for development.

## Installation
Use `npm install` to install the dependencies.
```
$ npm install
```

## Start-Up
Start-Up the server by running
```
$ node app.js
// or nodemon if installed too
$ nodemon app.js
```

## Usage
Below are the methods, route, the user, and reference to the controller and auth function that performs every action.

Method | Route | Controller | Auth
-----------|-----------|-----------|-----------
get | / | allFoods | -
post | /signup | newUser | -
post | /login | login | -
put | /updatepassword | updatePassword | decodeToken
post | /requestpasswordreset | requestPasswordReset | -
post | /resetpassword | resetPassword | -
get | /:id | userProfile | decodetoken
put | /edit | userUpdate | decodeToken
delete | /:id | delUser | decodeToken
get | /food/all | allFoods | decodeToken
get | /food/:id | aFoodDetails | decodeToken
get | /user/cart/ | allCartItem | decodeToken
post | /user/cart/:id/:qty | addTocart | deodeToken
put | /user/cart/:id/:qty | editCart | decodeToken
delete | /user/cart/:id | removeFromCart | decodeToken
post | /user/ordering/ | checkout | decodeToken
get | /user/ordering/ | orderHistroy | decodeToken
post | /admin/ | newFood | decodeToken, isAdmin
get | /admin/allfoods | allFoods | decodeToken, isAdmin
post | /admin/makeavailable | makeFoodAvailable | decodeToken, isAdmin
post | /admin/makeadmin | makeAdmin | decodetoken, isAdmin
delete | /admin/:id | deleteFood | decodetoken, isAdmin

### Order Information
Quickly create test users with the [createUser.js]() file by **uncommenting** the last line in app.js file to have `require("./createUser")`

```
...
module.exports = app
//  require("./createUser")      
```
In the console you would get this same message
```
Here is the login details for admin, email: admin@testmail.com, password: Password&123
Here is the login details for user, email: user@testmail.com, password: Password&123
```
You can use those details to start.
