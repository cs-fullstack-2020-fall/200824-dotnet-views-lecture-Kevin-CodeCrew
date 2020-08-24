# 200824 .NET Views Lecture

### Set Up
- Create a new .NET MVC app called Lecture using the .NET CLI
- Run the application without debugging
- View the application in the browser
- Create a new postman collection for the application

### Code Together
- Create an `Example` controller that extends the base Controller class from `Microsoft.ASPNetCore.Mvc`

##### Content Review
- DisplayContent Method : get method that returns a string
- DisplayUserContent Method : get method with one param that returns a string using that param

##### Index
- Index Method : get method that returns associated view by method name
- Index View : cshtml file in Views/Example directory that display an h1 with the text `Example Controller Display Content Method` and uses default layout and styling

##### Display User Info using query params and views
- DisplayUserView Method : get method with one query param that sends param to associated view using `ViewData` dictionary 
- DisplayUserView View : cshtml file in Views/Example directory that display an h1 with the text `User : [USER]` using the data passed from method

##### View All Users From a List
- User Mock Data : create a list of 3 users using a User struct with properties `id` and `name`
- ViewAllUsers Method : get method that passes list of user to associated view using `ViewData` dictionary
- ViewAllUsers View : cshtml file in Views/Example directory that loops through and displays both properties of users in user list passed from method

##### View One User From a List using LINQ
- ViewOneUser Method : get method that finds a user based on id query param and passes the id and name of the found user to the associate view using `ViewData` dictionary
- ViewOneUser View : cshtml file in Views/Example directory that display an h1 with the text `User Name : [NAME] User ID : [ID]` using the data passed from method

##### Add and Delete a User From a List
- AddUser Method : post method that creates a new user from information passed in the body, adds the new user to the user list, and returns the ViewAllUsers view with the updated list
- DeleteUserMethod : delete method that removes a user from the list of users and returns the ViewAllUsers view with the updated list

### Resources 
- [Docs](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/overview?view=aspnetcore-3.1)
- [Launch Code YouTube Video](https://youtu.be/H2Nf0w-YKcE)