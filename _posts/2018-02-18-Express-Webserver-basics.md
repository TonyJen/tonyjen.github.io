---
layout: post
title:  "Express web server basics"
date:   2018-02-17 00:14:52 -0500
categories: express
---

While creating a blockchain, I had to create web servers and also using Express for Node. That got me thinking that I should explain the basics of Express web server. 

Express is a framework that sits on top of Nodejs. It behaves like a web interface for application to hook into. 

![Express Diagram](/assets/Express Server.png){:class="img-responsive"}

Here is a basic express route with a get and post route.

<script src="https://gist.github.com/TonyJen/f7e1dc40b4ba2e8c7e47f4a01b56fff7.js"></script>

Notice req is the request package send to the web server and res is the response return from the server.

So that is how a basic Express server works, adding to this, we can then add routes and create the Blockchain application from this setup.
