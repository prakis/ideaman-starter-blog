---
title: Quickest way to develop MVP (using Firebase)
date: 2020-07-19T10:27:23.148Z
tags:
  - firebase
  - saas
  - cloud
  - lambda
draft: true
---
I will discribe my experience in building a mvp quickly.

The fastest way to develop a web app with userlogin and user maintaince is by using Google Firebase. Even big sites like IndieHackers.com using Firebase authentication mechanism.

For any clientside user data extraction(ex getting the user information) firebase provides wonderful javascript libraries to do the serverside actions. This is very unique to Firebase. Lets say you want to store some user info in the server database, you don't need write any serverside code, you can do all that from javascript (from inside the browser).

Firebase provides two types of database 'Realtime Database' (will mostly be deprecated sometime in future) and 'Firestore Database'. 

Few things to know about Firestore: Each document inside the firestore can be max 1MB. That doesn't limit how much data you can keep, **also any collection inside the document doesn't count for that 1mb size limit.**

For cloud storage (AWS S3 equalent) firebase provides Firebase Storage (Firebase storage is same as Google Cloud Storage, the main difference is firebase storage is easy api and limited fetures). If you create a bucket with firebase storage it is actually created as a Google Cloud Storage bucket.

Serverside functionality. Firebase Functions (equalent to AWS Lambda functions) you can write some functions which can be triggered from javascript(ajax) or from other saas apps, rest api. And most importantly you can also trigger a function on events, Like when some data changed in the firestore database you can trigger a function.

And about Firebase rules. If you can access user data from the browser, anyone can also access the complete user data. To avoid that Firebase provides Rules which provides some restrictions on the data, eg what data a particular user can use. Becauase of rules you can avoid lot of server side code. Rules are powerful.



Disadvataes of Firebase: most of these things are very proprietry to firebase so big issue is vendor lockin. It is alot of work to move from one Cloud provider to other. Firebase got generous free tier but their storage and other prices are on par with AWS pricing. It can go up quickly.

The one great thing about Google Cloud and Firebase is its lot easier to setup things than compared to AWS S3.