### In this walk through I will attempt to explain the function and what each of the files listed are responsible for in these folders. 

## Develop\config\middleware
\isAuthenticated.js: 
	This file handles registered and unregistered users and redirects them accordingly.  

## Develop\config
\config.json: 
	Acts as the configuration and setup for the mySQL databases.  

\passport.js: 
	This runs upon loading the page and serves as a method for checking if a user is registered or not.   

## Develop\models
\index.js: 
	Gathers required node packages & handles sequelize setup. This file connects to the config.json file to get and execute the database connection settings.

\user.js: 
	Creates our user account or information. This JavaScript uses bcryptjs to hash out the password in the database to protect user’s login account info. 

## Develop\public\js
\login.js
	Gets the data from the login form (email and password). This information is passed through the loginUser function and If the user has logged in before or registered than that user is redirected to the members route.

\members.js
	This js file looks up the information about the logged in user from the API and returns the value of the database for .member-name.

\signup.js
	This js file performs similar to the login file but instead of signing in an existing member this redirects the user to a sign up page for creating an account.

## Develop\public
\login.html
	This is the html template used for the login page. The page provides form input for the user to enter their username and password. 
    If the user is not yet registered than they are redirect to the signup page.

\members.html
	This is the html template used for the members’ page.

\signup.html
	This is the html template used for the signup page. Allows the user to enter in email and password.

## Develop\routes
\api-routes.js
       The file defines what API routes are available for use in the application. 

\html-routes.js
	This file handles the routing to the correct html files. As well as handling redirecting authenticated vs non-authenticated users.

## Develop\server.js: 
    This file is executed through a terminal window to begin running on our server as well as executing the app|site|code.

## Develop\package.json: 
	This file lists all the packages and dependencies necessary to run the code and have it function correctly. Without these packages installed the code will break and not function accordingly.  Some of the packages needed are sequelize | mysql2 | express | passport.

