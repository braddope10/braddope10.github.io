---
layout: post
title:      "JavaScript Fetch Requests Are Your Friend."
date:       2020-08-09 08:39:43 +0000
permalink:  javascript_fetch_requests_are_your_friend
---


**Why would I use fetch requests?**

Fetch requests or "AJAX requests" are pivitol for creating requests and responses from a specific endpoint or path where all of your objects will be handled and eventually used to manipulate the DOM. 

For example, let's say you want to gather all of the data from an API (Application Programming Interface) that contains the name and age of all the actors in the hit TV show "The Office" and list them by age, least to greatest, in your application. Instead of hardcoding multiple actor objects along with their desired attributes and waste time on repetative code, the easiest way to go about it would be to create a function in JS and assign it the task of fetching the data from the API directly. Saving you valuable time.

**How do I make a fetch resquest?**

Lets start by introducing you to a barebones fetch request.

* fetch('http://example.com/movies.json')
*   .then(resp => resp.json())
*   .then(data => console.log(data));
	
Now that you've seen what it looks like, lets pick it apart line by line to make sure you know how the fetch request is performed. 

* fetch('http://example.com/theofficeactors.json')

Line one is fairly simple, type 'fetch' and assign the correct path to the resource you want to fetch as an argument. The argument is manditory, so don't forget it. 

*   .then(resp => resp.json())

Line two then takes the response object and JSONifys it. Generally, this line tends to be very cookie cutter. This will return a Promise.

*   .then(data => console.log(data));

Line three then tries to resolve the promise and extract the data, which is our goal! This line will return your actor objects that you would have needed from the API. 

Finally, line four is where you do something like create the actor list we talked about or do whatever you would like with the fetched objects. This is where your OOP (Object Oriented Programming) comes into play.

Looks like you now know how to make a fetch request! Time to put it to use.

*Don't forget that there are many other ways to use fetch! You can use them for mulitple scenarios, like creating, updating, or even deleting those same fetched objects. Using fetch now allows you to access objects anywhere in your JS code.*

Resources:
* https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API
* https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch
* https://developers.google.com/web/updates/2015/03/introduction-to-fetch
* https://javascript.info/fetch
* https://scotch.io/tutorials/how-to-use-the-javascript-fetch-api-to-get-data
