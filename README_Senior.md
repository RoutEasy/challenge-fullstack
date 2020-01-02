# Senior MEAN Stack Developer Challenge 
## Description
Assuming you have finished our Fullstack Challenge, it is time to improve it a bit. 
Choose at least TWO of the topics below and implement them. If there is any topic uncover, describe it in details how would you implement them.
### 1. Automated Tests
> We know that automated tests is required to deliver a good application. Sometimes it seems to take a lot of time from coding, but it can help when a bug occurs.
We would like you to show your code testing and the automatomation of api calls skills - for that you could mock externals dependencies like geocoding and other api calls.
You can use any test runner and assertions libraries. We are expecting that you approach all use cases and unit tests. It is not required automated tests for the frontend, but would be a really 'nice to have' feature.
### 2. Continuous Delivery
> Continuous delivery helps DevOps and developers to deploy faster solutions and improvements to live applications, beyond that it ensures that everything is going to be alright when becomes to dependencies versions, automated tests and code quality.
Show us an automated deployment workflow that can be deployed easily from any device (mobile not needed). Make sure to install dependencies, show how you would run tests (if you have not implemented them yet) and bundle it.
### 3. Implement it as a Microservice
> Microservices are turning common sense these days. Netflix™ has shown how it built their entire solution on microservices, we believe that it can be a great alternative to monolithic solutions and improve the developer's quality of life.
We suggest any integrated solution on the Challenge that will lever its sophistication such as:
- Single Sign On
    > Authenticate using a microservice. You **can not** use an entire 3rd party API like Facebook™, Google™ etc., but you can use encryption libraries and external dependencies as you wish.
- Queue
    > Deliver a queue to ensure all requests reach the OrderApi from your Challenge. Persist it anywhere you want, in-memory, NoSQL database etc.
- Implement the [Workflow feature](https://github.com/RoutEasy/challenge-fullstack/blob/master/README_Senior.md#4-workflow-engine) as a microservice, and if you do so we will consider it as two features.
- Be creative!
    > Improve your Challenge with any feature you think that will surprise us. Be aware that we are going to be tough in your evaluation. Ensure us that you will show what you are capable of.
### 4. Workflow engine
> Workflows are very present in our day-to-day. Statuses gives the user feedback on what is happening and helps manage actions to ensure that the operation succeeds.
Show us a nice and S.O.L.I.D. 'orders' workflow. Implement the following statuses to the 'orders' and display it to the end user:
```
- On Hold -> The order is waiting to be delivered
- On Route -> The order is going to the destination
- Checked-in -> The order has arrived
- Completed -> The order has been delivered!
```
> The user needs to be able to execute actions to change the order's next status. You should implement an automated change to status to simulate our current application and the interactions between our mobile and web app. Those actions can occur randomly or each minute. The statuses screen should be updated with those actions.
