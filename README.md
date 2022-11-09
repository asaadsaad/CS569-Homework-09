# CS569 Homework
## Angular Reactive Forms
Use the [Request Response API](https://reqres.in/) and build an Angular application with the following features:
* List all users
* Add new user
* Update user by ID
* Delete user by ID
  
**Notes**
* Type all responses according to the API.  
* Use Angular Router and Reactive Form Modules.
* The API does not add, update, delete your data. However, you will need to update your state as if it were doing so.
  
**Optional Requirements**
* Use the API to register and login and save the user state globally, then only allow using the above features only after they login. 
  
**Working with featured module**
* Create a `UserModule` (ng g m user)
* Add the `RouterModule` to both `AppModule` and `UserModule`
* Convert `AppComponent` to a template, and a router link to go to 'users'.
  
Configure `AppModule` router to display:  
* `WelcomeComponent` by default
* Load `UserModule` dynamically once the route says 'users'
  
Configure `UserModule` router to display:  
* `ListUsersComponent`
* `AddUserComponent`
* `UpdateUserComponent`
  
Create a `UserService` within `UserModule` that's provided at root  
Add `HttpClientModule` to `AppModule`
Add `ReactiveFormsModule` to `UserModule`  
  
`AppModule` should look like this:
```javascript
declarations: [AppComponent, WelcomeComponent]
imports: [BrowserModule, HttpClientModule, RouterModule.forRoot()] // configure the router to load the UserModule in Lazy way
```
UserModule should look like this:
```javascript
declarations:[ListUsersComponent, AddUseComponent, UpdateUserComponent]
imports: [CommonModule, ReactiveFormsModule, RouterModule.forChild()] // configure the router to load each other components above on different URLs
```
Remember:
* we need `BrowserModule` in `AppModule`, and `CommonModule `in all featured modules (Hybrid)
* we need `RouterModule.forRoot()` in `AppModule`, and `RouterModule.forChild()` in all featured modules (Hybrid)
* we need `HttpClientModule` only once in `AppModule` (Service-Based)
* we need `ReactiveFormsModule` in every module that requires forms (Component-Based)
