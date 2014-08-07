---
layout: post
title: "Core Technologies Used in Treepie Products"
date: 2014-08-07 15:03:15 +0530
comments: true
categories: 
author: Ningsuhen Waikhom
---

At Treepie, we develop products which will be used by millions of people around the world. When millions of people are using it; performance, robustness, efficiency, etc. are not to be taken granted. Choosing the best technologies suitable for our products was an interesting piece but not an exact science. 

There's no written page in Wikipedia which says choose this technology especially when it comes to Web Applications. Even if you go to Quora or StackExchange(Stackoverflow), there's always some guy who is ready to kill for Ruby on Rails and some another guy who lives, eats and drinks Java (or java based frameworks like Play).  I personally had more experience in Django which, by the way,  I would love to use. However, it's one of the biggest decisions for a startup and after some research and trials, we came to the final decision of our core technologies. Let's have a look at the technologies used at Treepie as of today, 7th August 2014.

##MEAN - MongoDB, Express, AngularJS & NodeJS
Yes, we chose MEAN. It stands for MongoDB, ExpressJS, AngularJS & NodeJS. There are two MEAN frameworks - mean.io & meanjs.org. Both are started by the same guy - [@amoshaviv](https://github.com/amoshaviv), see this [discussion on stackoverflow](http://stackoverflow.com/questions/23199392/difference-between-mean-js-and-mean-io). Apparently, there were some conflicts between the members of the original MEAN framework and the original creator [forked out of the conflict](http://blog.meanjs.org/post/76726660228/forking-out-of-an-open-source-conflict). This is not a new thing if you like open source softwares. Now, let's get back to WHY we chose MEAN. 

It won't be wrong to say MEAN is just a collective name we give to the individual technologies. The reason why we chose MEAN was majorly driven by the individual technologies. So, let's dive into why we choose these technologies in the first place.

###MongoDB
MongoDB is new hot chick in town. Today's web and mobile technologies are based on progressive, flexible and rapid release cycles which you can call agile. SQL is not something I prefer these days for it is not flexible enough for agile process. To prevent discussing the SQL vs NoSQL topic here, I'll recommend you to see [this](https://www.google.co.in/webhp?sourceid=chrome-instant&ion=1&espv=2&ie=UTF-8#q=sql%20vs%20nosql). Now, the question is to choose which NoSQL database. Back in Adobe, out team evaluated these MongoDB, Cassandra, CouchDB & if I'm not wrong, HBase. Ultimately, our team chose MongoDB. So, in good faith, I was inclined to use MongoDB. But this [comparison](http://kkovacs.eu/cassandra-vs-mongodb-vs-couchdb-vs-redis) made more sense. Considering the fact that our database will change all the time, as users sync their contacts, MongoDB is the winner for us. 
>**Best Used:** If you need dynamic queries. If you prefer to define indexes, not map/reduce functions. If you need good performance on a big DB. If you wanted CouchDB, but your data changes too much, filling up disks.

>**For example**: For most things that you would do with MySQL or PostgreSQL, but having predefined columns really holds you back.

###Express
The decision to choose [Express](http://expressjs.com/) is primarily because of two reasons - NodeJS & familiarity. The team was familiar with express though not experts. We liked the way it works. Middle-wares make it easy to intercept requests at any level and pre or post process them. Most of the Nodejs modules are based on Express. It's a key component of the MEAN frameworks. In short, it is the most popular web application framework in NodeJS. Although we did bump into [Restify](http://mcavage.me/node-restify/), which seemed like a good fit for REST APIs, we chose Express for the reasons mentioned above.
 
###NodeJS
Choosing the Web Application was the toughest decision. Apart from being the core programming language, changing the Backend language is the hardest thing to do if we happen to hate it in the future. Also, the team had experience in varieties of programming languages including Java, Python, PHP, etc.  

**Ruby on rails** is something we would have wanted to use but we had heard enough people complaining about its performance and yes, we had no first hand experience on it.  **Java** again is awesome but isn't it too much for startups? My Experience with Java is that I write too much code to do something so small that I just feel like it's a waste of time. (No offense to Java lovers. It's just a personal opinion. There are of course so many good things about java.) So, we were down to 2 Programming languages - Python and Javascript (NodeJS). The Duel was a tough match.

Few months before this, i had used NodeJS and I wasn't a big fan of it. As a Django developer, i liked the ability to spin off a new app quite quickly. The app contributions of Django are quite good and I suggested using Django. But we eventually decided to try out both Django and Nodejs. Since Django is more of a framework, we did a little bit of research for a similar thing for Nodejs and MEAN came up. Let's see how the comparison between Django and MeanJS turned out.  

|Django|MeanJS|
|------|------|
|Doesn't support MongoDB by default|MongoDB is the default Database of most Nodejs Frameworks| 
|Third party modules like [Django-Nonrel](https://github.com/django-nonrel/mongodb-engine) & [django-mongo-engine](http://django-mongodb-engine.readthedocs.org/en/latest/) were not convincing enough as the Django Developers were still focused on SQL|MongoDB being a JSON(BSON) based datastore, MeanJS or rather NodeJS works better with MongoDB than no other Datastore|
|Django is still a website framework.|MeanJS is a Web Application Framework|
|Although you can have REST APIs, the developers still appear to be focused on websites rather than web applications or SPA|MeanJS is designed using mostly REST APIs|
|Django in fact doesn't play very well in Single Page Applications|AngularJS comes by default and works perfectly|
|Many Django apps work with cookies and are tightly coupled with client side renderer|The web front-end is so loosely coupled with the backend that we could easily split the client code into a different project |
|Python & Javascript Developers needed|Only Javascript developers needed|

All in all, we decided to go with NodeJS. And believe me, I'm get surprised almost everyday with the cool things that NodeJS can do. I'll write about the cool new things that NodeJS can do in my next post.

###AngularJS

