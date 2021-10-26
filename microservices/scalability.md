# Scalability

Scalability is one of the top concerns when it comes to designing software systems. Applications are generally created with the objective that someday there will be a large number of users using them. 

However, the initial application does not need to support a large number of users. It needs to expand when necessary but overall keep the cost low as long as it can.

## Definition

> "Scalability is the measure of a system’s **ability** to **increase or decrease** in performance and cost **in response to changes in application and system processing demands**."
> > -- <cite>Gartner</cite>

Let's reiterate the keywords:
1. Ability - As stated earlier, does not have to be super strong at the beginning, but should be able to evolve when needed.

2. Increase or decrease - Upwards isn't the only direction. To optimize the cost, it needs to shrink too otherwise we will be spending more on resources and reducing our profits.

3. In response to changes in demand - Demand can be divided into two parts. It's not only the users that can increase, but we also want to occasionally add features. The application needs to monitor the impact of user/feature changes and scale accordingly - whether automatically or through manual intervention.


## Types of scaling

Imagine that the house(the resource) you're living in was turning out to be smaller for your needs. People(users) in the house increase as life goes on and furnitures(features) increase too as the standard of living goes up. Now you want to expand your house for comfort. There are typically two options

1. Upwards - You decide to create another floor above your house and it solves the issue. This is called **Vertical Scaling**. The users and features remained at the same location but they had a bigger resource supporting it. This is typically equal to adding more physical resources(CPU/Storage/Network upgrages) to an existing server so that it can perform well against increase in demand.

However, you cannot keep creating another floor every time you need to expand. Someday, the strength of the  house will become a limitation. In the same way, the limit to which physical resources can be increased is also fixed. Lets look at another way to tackle this problem.

2. Outwards - You decide to buy/create another apartment and some of your family members and their things can shift into it. This is called **Horizontal scaling**. You increase the resources so that the all the load does not come to one resource. This is achieved by adding servers with similar capabilities and a load balancer which divides the user requests among servers.

Now the problem and limitations that we had with vertical scaling is removed in horizontal scaling, we can buy as many apartments as we need (assuming that the apartments are available...but not overthinking it further)

As much as horizontal scaling looks better and efficient in long term, it is not always the easier and certainly not the cheaper option between the two types of scaling. 

We will compare the two options but before that let's understand what is being scaled here.

## What are we scaling?

An application is generally created using multiple software components. We talk about tiered architectures. Most of the applications are created using some variation of 3-tier or N-tier architectures. If you want to learn/revise these architectures, check out this [thread by Jon Jackson](https://twitter.com/iamjonjackson/status/1448261875947425793)

{% twitter 1448261875947425793 %}

Note: You may have heard about Microservices architecture. For all practical purposes, a single microservice is an application in itself and has a N-tier(N>=2) architecture of its own. Just like a slice of Pizza is also a Pizza and contains all the same layers.







