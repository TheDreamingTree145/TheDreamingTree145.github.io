---
layout: post
title:      "Popular Rails Generators"
date:       2018-01-22 23:08:36 +0000
permalink:  popular_rails_generators
---

One of the best parts of Rails is how much code you don't have to write. Rails comes with different genterator commands that can be run from terminal similar to generating a rails app. The command to run a generator is:

`rails generate GENERATOR [NAME] [OPTIONS]`

There are about 10-15 different generators, but we will cover the most common.

### Migration
Running a migration can create a migration file for you. For example if we had a author model and wanted to add a column with a name of birth_year, we could run a migration that looks like this:

`rails generate migration add_birth_year_to_authors:date`

Running this migration will create a correctly named migration file that just needs to be told what needs to be done.

### Model
This is probably the most used generator. Running the model generator will create a few files for you. The most importants are the model file which is inheriting from ActiveRecord and the migration file for adding the model table to the database.

### Controller
The controller generator is also very popular. The controller generator will create a lot of files for you! It will create the controller file along with routes specified in the options of the generator, all of the views for the associated routes, a cofferscript file, a scss file and  a helper file. Controller generators are generally not great when used for building a CRUD interface because we will end up with some unneeded views when adding in the create, update and destroy actions.

### Resource 
The resource generator encompasses much of the functionality of the previous generators, but it gives us a bit more flexibility and can be used well with a CRUD interface. To run a resource generator:

`rails generate Resource MODEL [OPTIONS]`

This is generator will create everything the controller and model generators will create except for a few things. Resource will create a view directory, but not the associated templates. However, a resource generator will be based on the CRUD interface so it will create a full resource for the model in routes.rb.

### Scaffold
Finally, we come to the grandaddy of generators. The scaffold generator. This generator will do everything a resource generator does and more. It will create a full set of CRUD views, without the unnecessary views, JSON builders. It will also have some code in all of your views and your controller, so after running a migration you will actually have a fully functioning basic crud app.

### Conclusion
Generators can be very powerful and helpful when working on a rails application. It's important to not become too reliant on generators, especially the larger ones such as the Scaffold. That said, when used properly they are one of greatest parts of rails and save a lot of time.

