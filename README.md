# CS569 Homework 10
## Angular Reactive Forms
You app will show a link `Feedback` that lazy-loads the `FeedbackModule`.  
  
Create a lazy-loaded module `FeedbackModule` that displays a reactive form to allow users send their feedback. The form includes the following fields (`fullname`, `email`, `address`, `phone`, `type`, `message`), the `type` field has the following values: `question`, `feedback`, `complaint`, `suggestion`, `inquiry`.  
  
**Form specifications**
* `fullname` should have at least two words separated by a space. 
* `email` to be a valid email.
* `message` has to contain at least 100 chars. Display the remaining chars.
* All fields are required. `submit` must only be activated when all form restrictions are met.
* Log the form value in the console. 

