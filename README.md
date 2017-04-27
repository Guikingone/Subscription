# Subscription pattern

This repository contains the logic and examples about the Subscription pattern.

## Introduction

Welcome everyone, glad to see you here, first, why are you here ?

simple question with a simple answer, we're here for discovering a new pattern and probably, a good one, in order to be simple, let's
see what this pattern is, how can we implement it and how it works.

## Logic

Alright, has you know, web development have come a long way, first, we use new technologies and we try to build
the best user experience (in the visual like in the performances aspect), this way, we need to solve a lot of problems
and most of them are about performances, how can we make our pages faster ? How can we make this pages as fast and simple as light ?

In fact, today, frontend developers have some solutions, they use SPA logic and async task in order to solve the problem of performances and
scalability, this way, the client is build is Javascript and all the 'hard' logic is dispatched from the server to the client, simple approach
and simple logic.

For now, as a backend developer, I grown up with the idea that we can't build a fast backend natively, it was the truth earlier with the
old school frameworks and the server to client system, as I discover later, you can build a faster and smoother backend with PHP, that's
the truth, don't misunderstand my words, I'm not on the way to tell you that PHP is faster than Javascript
but we can improve drastically his performances and scalability.

First, some history.

**_From where comes the Subscription pattern ?_**

In fact, from frontend logic, specially from Meteor who use NodeJS like no one and who's able to build lightning-fast applications,
he build his logic from NodeJS and add a full stack logic (like BDD, Session, Image management, Email and others) in order to ease
the process.
As I discover earlier, Meteor is capable of managing full-stack apps with a simple and pretty solid code, yes, I'm not telling you some
bullshit, Meteor is capable of handling hard and multiples request with a minimal code !

**_But, what's the point with PHP ?!_**

In fact, Subscription is based on the BDD logic used by Meteor, by meaning this, I mean, we use the "concept" and not the whole package !

Let's explain what's the concept.

In Meteor, when you use MongoDB (who's included natively), you use 2 phases, first, the frontend receive the request (for reading, updating or creating)
the resource, then, he check if the backend has already the information, if not, the backend is called and updated with the frontend request, simple things
here but let's explain where this logic is cleaner.

Let's imagine that you have submitted a form and you need to show as fast as possible the result in the frontend, Meteor handle the request
and update the frontend "server" (in fact, let's compare this to a callback), the frontend server contains the status of the Mongo Documents at the time
you do the request, this way, your frontend is up to date to the last modifications, problem is, your backend don't know about this update at this time
and you can encounter some problems about documents logic, for this, Meteor made a asynchronous request from the frontend to the backend logic and update
the Mongo document in the backend, this request is completely masked and your frontend continue to keep the mongo document up to date
with the data he receive.

That's the theory.

**_But, what's the point with our backend logic ?_**

## Schemas

## In-Depth