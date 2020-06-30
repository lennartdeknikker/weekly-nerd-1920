# The possibilities of serverless functions
**Lennart de Knikker | June 30th 2020**

A few weeks ago, I attended the online JAM stack conference. One of their speakers was Jan van Hellemond. He spoke about the advantages of serverless functions and about how he managed to set up online ticket sales without servers, frameworks or cookies. At first I thought this would be a bit ambitious, since the sale of tickets is something that has to happen in a secure way, minimizing risks like that of losing peoples data or selling too many tickets. It also made me curious, so I kept watching. Eventually, he talked about the use of serverless functions, which, in combination with some other technologies, made it possible to even deploy changes to production during peak load.[(1)][1] I had heard about serverless functions before and recently I had seen that Netlify, the host of this conference, rolled out their own serverless services.[(2)][2] I got interested and tried to find out more to see if I could use this for my own projects.

## What are serverless functions?
*Serverless functions*, also known as *Functions as a Service (FaaS)*, allow us to deploy functions or little pieces of code and have them run independently. These little pieces of code are also called *microservices*. [(3)][3]

In an interview by Forrest Brazeal, Steven Faulkner (engineering lead at Azure Cosmos DB) defines serverless functions as follows:

> The way I describe it is: functions as a service are cloud glue. So if I’m building a model airplane, well, the glue is a necessary part of that process, but it’s not the important part. Nobody looks at your model airplane and says: “Wow, that’s amazing glue you have there.” It’s all about how you craft something that works with all these parts together, and FaaS enables that. [(4)][4]

I think this analogy also explains the importance of these functions. Serverless Functions form an indispensible part of most applications that use them. Even though glue is no visible part of the airplane, without it, the airplane wouldn't be able to fly. It could as well crash.

That brings me to my next question:

## Would it be a good idea to leave the responsibility for vital parts of your application to a service you're not completely in control of?

FaaS is offered by multiple companies, the most used service being Amazon Web Services (AWS) Lambda. As stated in their documentation:

> AWS Lambda is a compute service that lets you run code without provisioning or managing servers. AWS Lambda executes your code only when needed and scales automatically, from a few requests per day to thousands per second. [(5)][5]

This definition brings to light one of the flaws as well as one of the advantages of serverless functions. Because it scales automatically and runs only when needed, you won't have to worry about those things. On the flip side, it also takes away your control. You won't be able to monitor any errors and you'll depend on the provider of the service to keep the vital parts of your application working. [(6)][6]

You'll have to decide for yourself whether this lack of control is worth the advantages. I think in most cases, because these microservices run independently, serverless functions are actually more reliable than when you would set up your own architecture. As said in my introduction, FaaS  for example makes it possible to deploy changes to your application, even during peak load, without affecting any of your microservices.

As Faulkner also pointed out in the forementioned interview, it's also possible to emulate these serverless functions locally. This can partly solve the problem of not being able to monitor errors as well.[(7)][6] You could for example use [serverless-offline](https://www.npmjs.com/package/serverless-offline) to do so.

## What would I use serverless functions for?
A few use cases for serverless functions, provided in Netlify's documentation are
- interaction with protected APIs like databases or payment services
- image handling
- searching large amounts of data[(8)][8]

These use cases are good examples, because these are things you would want to run on-demand and return results just like an API does without exposing underlying code.

## Conclusion
When I want to have a lot happening serverside and I want to have full control I would still be inclined to just set up my own express server. When I build a simple website that just needs a few functionalities that would better not just run in the clients browser, whether that is due to reasons of security or when you can't rely on users having a powerful enough browser to run the code, I think it would be nice to try out serverless functions and see if those can help me out.

## Sources
1. https://www.youtube.com/watch?v=gUjmXnkWvww
2. https://functions.netlify.com/
3. https://medium.com/hackernoon/a-crash-course-on-serverless-with-node-js-632b37d58b44
4. https://read.acloud.guru/serverless-is-eating-the-stack-and-people-are-freaking-out-and-they-should-be-431a9e0db482
5. https://aws.amazon.com/lambda/resources/?aws-lambda-resources-blog.sort-by=item.additionalFields.createdDate&aws-lambda-resources-blog.sort-order=desc
6. https://read.acloud.guru/serverless-is-eating-the-stack-and-people-are-freaking-out-and-they-should-be-431a9e0db482
7. https://read.acloud.guru/serverless-is-eating-the-stack-and-people-are-freaking-out-and-they-should-be-431a9e0db482

[1]: https://www.youtube.com/watch?v=gUjmXnkWvww
[2]: https://functions.netlify.com/
[3]: https://medium.com/hackernoon/a-crash-course-on-serverless-with-node-js-632b37d58b44
[4]: https://read.acloud.guru/serverless-is-eating-the-stack-and-people-are-freaking-out-and-they-should-be-431a9e0db482
[5]: https://aws.amazon.com/lambda/resources/?aws-lambda-resources-blog.sort-by=item.additionalFields.createdDate&aws-lambda-resources-blog.sort-order=desc
[6]: https://read.acloud.guru/serverless-is-eating-the-stack-and-people-are-freaking-out-and-they-should-be-431a9e0db482
[8]: https://functions.netlify.com/


## Further reading
- [The hidden costs of serverless](https://medium.com/@amiram_26122/the-hidden-costs-of-serverless-6ced7844780b)
- [A crash course on Serverless with Node.js](https://medium.com/hackernoon/a-crash-course-on-serverless-with-node-js-632b37d58b44)
- [6 things I’ve learned in my first 6 months using serverless](https://read.acloud.guru/six-months-of-serverless-lessons-learned-f6da86a73526)
