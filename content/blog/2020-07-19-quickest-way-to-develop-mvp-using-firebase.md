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