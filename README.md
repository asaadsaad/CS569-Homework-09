# CS569 Homework 7
## Angular Reactive Forms
Complete  full CRUD operations and build Rest API for an entity `Addresses`:   
```javascript
{
  _id: ObjectId(), 
  street: string, 
  city: string, 
  state: string, 
  zipcode: number, 
  location: {long: number, lat: number}
}
```
Build an Angular project using Angular Router and Angular Reactive Forms to manage addresses and meet the following requirements:  
* List all addresses `{path: '', component: ListComponent}`, each address should have a button to delete the address by `_id`.
* Add a new address `{path: 'add', component: AddComponent}`
* Edit an existing address `{path: 'edit/:address_id', component: EditComponent}`) 
  
**Other Requirements**
* Assuming that all fields are required, create an asynchromous validator to check that the `zipcode` is unique.  
* Create a `checkChrome` guard to be applied on `EditComponent`, which uses a service `CompatibilityService` and [checks](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/userAgent) if the app is working on `Chrome` version 100+. 

