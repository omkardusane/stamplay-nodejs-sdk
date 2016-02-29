<img src="https://editor.stamplay.com/img/logo-robot-no-neck.png" align="left" width="170px" height="160px"/>
<img align="left" width="0" height="160px" hspace="10"/>

> #Stamplay NodeJS SDK
[![npm version](https://badge.fury.io/js/stamplay.svg)](https://badge.fury.io/js/stamplay)
[![Build Status](https://travis-ci.org/Stamplay/stamplay-nodejs-sdk.svg?branch=master)](https://travis-ci.org/Stamplay/stamplay-nodejs-sdk)
[![No dependecies](http://img.shields.io/badge/dependecies-0-blue.svg)](https://stamplay.com)
[![Code Climate](https://codeclimate.com/github/Stamplay/stamplay-nodejs-sdk/badges/gpa.svg)](https://codeclimate.com/github/Stamplay/stamplay-nodejs-sdk)

This library  gives you access to the powerful Stamplay cloud platform from your Node app. For more info on Stamplay and its features, see the <a href="https://stamplay.com">website</a>
<br>
<br>

##Getting Started
This module is available for download on NPM:

```
npm install stamplay
```

To get started: 
```javascript
var Stamplay = require('stamplay')
var stamplay = new Stamplay('appId', 'apiKey')
```

##How to use it
Register a new user:
```javascript
var data = {
	"email":"john@stamplay.com",
	"password":"john123"
}
stamplay.User.save(data, function(error, result){
	//manage the result and the error
})
```
Store data using Objects:
```javascript
var data = {
	"description":"A description",
	"title":"New title"
}
stamplay.Object('foo').save(data, function(error, result){
	//manage the result and the error
})
```

##Available components
This NodeJS SDK expose the following components:
 
* [User](#user)
	* <code>save(data, [callback])</code>
  * <code>get(data, [callback])</code>
  * <code>remove(id, [callback])</code>
  * <code>update(id, data, [callback] )</code>
* [Object](#custom-object)
	* <code>save(data, [callback])</code>
	* <code>get(data, [callback])</code>
	* <code>remove(id, [callback])</code>
	* <code>update(id, data, [callback])</code>
	* <code>patch(id, data, [callback])</code>
	* <code>upVote(id, [callback])</code>
	* <code>downVote(id, [callback])</code>
	* <code>rate(id, rate, [callback])</code>
	* <code>comment(id, text, [callback])</code>
* [Code Block](#codeblock)
	* <code>run(data, queryParams, [callback])</code> 
* [Webhook](#webhook)
	* <code>post(data, [callback])</code> 

Also this components the sdk have some support objects to help you in common operation:

* [Query](#query)
	* <code>greaterThan(attr, value)</code> 
	* <code>greaterThanOrEqual(attr, value)</code> 
	* <code>lessThan(attr, value)</code> 
	* <code>lessThanOrEqual(attr, value)</code>
	* <code>pagination(page, per_page)</code>
	* <code>between(attr, value1, value2)</code> 
	* <code>equalTo(attr, value)</code> 
	* <code>exists(attr)</code> 
	* <code>notExists(attr)</code> 
	* <code>sortAscending(attr)</code> 
	* <code>sortDescending(attr)</code>
	* <code>populate()</code>
	* <code>populateOwner()</code>
	* <code>select(attr,...)</code>
	* <code>regex(attr, regex, options)</code>
	* <code>near(type, coordinates, maxDistance, minDistance)</code>
	* <code>nearSphere(type, coordinates, maxDistance, minDistance)</code>
	* <code>geoIntersects(type, coordinates)</code>
	* <code>geoWithinGeometry(type, coordinates)</code>
	* <code>geoWithinCenterSphere(coordinates, radius)</code> 
	* <code>or(query,..)</code> 
	* <code>exec([callback])</code> 

-------------------------------------------------------

# One more thing
Go to [Stamplay](https://stamplay.com) and ENJOY!.
<img align="right" src="https://editor.stamplay.com/img/logo-robot-no-neck.png" height=60>

