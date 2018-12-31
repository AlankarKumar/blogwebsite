---
title: "Getting started with Mocha"
date: 2018-12-30T18:28:46+05:30
bigimg: [{src: "/img/mocha.jpg"}]
tags: ["mochajs","testing"]
---

## What do you learn?

* Setting up the environment for and installing MochaJS
* Understand what MochaJS is
* Write & run your first test using Mocha

## What's Mocha?

> It's a javascript test framework which offers BDD style tests.

## Why even bother using it?

* Runs on a very popular platform **NodeJS**
* It's really just a skeleton and can include loads of testing libraries for assertions, api calls, ui automation etc.
* Supports ES6 through babel
* And above all multiple reporting libraries exist for Mocha which produce prettified reports

## Let's SetUp the environment

The first thing you require is to have Nodejs installed on your system. You can find the installables [here](https://nodejs.org/en/download/).

Once you have installed Nodejs you migh want to check if it's correctly configured in your system.

### Just do it!

* Open command prompt/terminal on windows/mac or linux.
* Type `npm -v` and press return.
* It should give a version number.If it does, follow along!

To write tests in Mocha you need to have Nodejs project in which you can create `.js` files and write tests.

## How it's done?

We will use **VSCode** as our editor to write test. If you don't have it it would be a good idea to download and install in now. You can do so from [here](https://code.visualstudio.com/download).However you can use any editor of your choice.

Open a command prompt and type in below.


```
mkdir sampletest
cd sampletest
npm init
```

A bunch of questions will follow.Don't worry it's helping you setup the things.
To fastrack to writing tests let's leave everything to default by pressing return each time it asks a question.


![alt text](/img/npminit.jpg "npm init")

Once the `npm init` is complete you should have `package.json` file in your `sampletest` directory.

![alt text](/img/packagejson.jpg "package json")
## What next?

* We need to install `mocha`
* Create a `test/test.js` file
* And write a test

To install mocha run the following in a command prompt/terminal

```
npm install --save-dev mocha
```

This downloads mocha from npm registry servers into your `node_modules` directory

The `--save-dev` flag is to inform `npm` to install `mocha` as a development dependency.If it is not making sense to you right now, you can just ignore this detail.

**Good you have persevered so long.**
**All what is left to do is write a test**

To do this in you project folder type in(Alternatively, you can use your Code editor to do the same)

```
mkdir test
cd test
.>test.js
```

**Note: Ignore the error at command prompt in windows you should have `test.js` file created inside your `test` folder**

Copy & paste the code below in your `test.js` file
```javascript
var assert = require('assert');

describe('My first test suite',function(){
    it('My first test', function(done){
        assert.equal(1,1);
        done();
    })
})
```

* In the code above `describe` provides a way to organize your test suites. It's a placeholder for you main tests.
* The actual test code is written inside `it`.
* Both `describe` & `it` take anonymous functions as parameters & contain `it`s and testcode respectively.

What is `assert`?

It is Nodejs default assertion library to test invariants.

Why `assert`?

There are numerous libraries which perform this task like **chaijs**, **shouldjs** etc. They invariably make your task of performing assertion easier.But, the goal here was to get started with **mocha**. I will include more on this in future articles.

## Let's run the test

In you terminal from your project's root folder type the following:

```
npx mocha
```
You should get a output like below

![alt text](/img/mochatestrun.jpg "mocha test run")


**Congratulations! you just ran your first mocha test.**