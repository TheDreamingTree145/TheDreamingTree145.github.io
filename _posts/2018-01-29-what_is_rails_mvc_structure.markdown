---
layout: post
title:      "What is Rails MVC Structure"
date:       2018-01-30 00:34:02 +0000
permalink:  what_is_rails_mvc_structure
---

Even if you are just a beginner with Rails, at some point you have probably heard that Rails follows the MVC structure. There are many languages that have frameworks that follow the MVC pattern such as Java, PHP, and C. But what is MVC? MVC stands for Model, View, Controller. The main principle is that we have three very separate, but closely connected divisions or substyems. Each subsystem has specific responsiblities and parts of the application that is should handle and parts of the application that it should not handle.

## Model
The model is your business logic will go. Typically in rails you will see model classes inherit from ActiveRecord. This is the area where the application will handle the models relationship with the database.  This is the area where any methods that will effect models will go as handling validations, model associations and much more. The key here is to understand the model is where you will retrieve and change database data.

## Views
Views are where we put what we want to actually go on the page. The views should contain nothing more than presentation logic. Depending on you application, you may or may not need to use Ruby code in the views. Fortunately, if needed ActionView provides us with embedded Ruby or ERB. For many applications, this can act as a basic HTML page with JavaScript tags. Again, the key here is that the View is for presentation logic only.

## Controller
The controller is aptly named. This section of the MVC is really the glue that holds everything together. For example, if we have a model name User and we needed to display that information on our home page we would in the controller query the model to give us information from the database about a particular user. Then the controller would take the information provided by the model and get it ready to use in the view, usually using an instance variable. The controller handles the application logic.

## Finale!
So there's not really a grand finale to all this. These are the basics of a MVC structured application. There are defined patterns to follow, namely keeping in mind the separation of concerns. The Model controls the business logic, the Controller takes care of the application logic and the Views take care of presentation logic. Follow these principles and you are well on your way to being an MVC master.
