---
title: "The very basics of Flask User"
date: 2021-01-31T01:44:51+05:30
draft: false 
---

## Introduction to Flask

Before we delve into Flask-User, let's get to know a bit about the Flask (micro)framework. 
Developing static as well as dynamic web apps in Python is not a newfangled concept. There have existed several frameworks right from Zope(1998), CherryPy(2002), Django(2005), web2py(2007), Tornado(2009) and lots more. Django and Flask have undoubtedly been the leading frameworks since the past couple of years. There is a constant barrage of questions and comparisons to determine which among them is the "superior" framework. The major difference in my opinion, is how both of these frameworks present their applications to the developer. Django offers a more "complete" experience : a pre-package of admin side panels, an ORM (object relational mapping), and a proper directory structure. Flask on the other hand offers a more raw experience but focuses more on simplicity and control to give the developer the freedom to craft their own application. Despite the flexibility and independence, Flask still lacks the popularity that Django has achieved and continues to play as a second fiddle in the Python Web Dev universe.

Flask has a couple of dependencies namely Jinja and Werkzeug. Jinja is a template engine that basically generates HTML files with powerful features like macros and template inheritance. It is modelled after Django's templates but are not completely compatible with them. To put it very roughly, one of the major differences is that Jinja allows the user to write logic inside extensions which Django prohibits. Werkzeug (German word for "tool") is a WSGI (web server gateway interface) web application library. WSGI basically is a middleman between a web server (say an Apache or Nginx server) and the Python backend code. It provides a sort of common ground for Python frameworks to interact with the web.

Major commercial enterprises like Netflix, Reddit and Lyft are amongst the many companies that actively use the Flask framework.

So this part was about Flask - the framework, which this post isn't about. The question that arises next is...

## So what is Flask-User ?

Flask-User is a Flask extension which provides simple yet flexible user management. Events like logging in, logging out, email validations, sessions are handled by this extension. Written by Ling Thio in 2018, it offers an easier approach to build web applications involving users as comapred to creating the same in vanilla Flask.
