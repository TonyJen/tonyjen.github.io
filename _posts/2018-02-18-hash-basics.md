---
layout: post
title:  "Hashing basics"
date:   2018-02-17 00:14:52 -0500
categories: blockchain
---

Hashing in blocks is the corner stone in a blockchain application. A hash function creates data from user data. The special thing is that the created data is of consistent length, which makes comparing easy. 

Whether a data is a single character or a novel, the resulting hash is the same length. This have one key advantage, which is to make sure the data integrety is consistent across blocks and users. 

In node we can use a library called cryto-js, and a simple example is the following:

<script src="https://gist.github.com/TonyJen/7d01576b7f319f5f7fa70782ec3376f3.js"></script>

SHA256 is the function that takes any data and returns a hash. There you have it, a simple explaination of what a hash is and how to use it. 
