# Rails API Diagnostic

Place your responses inside the fenced code-blocks where indicated by comments.

What is the purpose of a backend?

```md
The purpose of a backend is to handle the incoming requests from the client and return the data necessary for the application to function. Typically this means interacting with a database.
```

Which layer in the MVC pattern is used by the controller to fetch data?

```md
The controller sends instructions to the model layer in order to fetch data from the database.
```

Which layer in the MVC pattern communicates with the model?

```md
The Controller is the only layer in the MVC pattern which communicates with the model.
```

Why don't we use views in our interpretation of the MVC pattern?

```md
We do not use views because we use serializers to perform the same function.
```

What does C.R.U.D stand for?

```md
C.R.U.D. stand for Create, Read, Update, Delete
```

In which part of the MVC pattern can we find C.R.U.D actions?

```md
C.R.U.D actions can be found in the Router, which translates them into framework-specific actions that the backend understands.
```

List at least 5 standard rails actions that C.R.U.D requests correspond to?

```md
Read: index, show
Create: create
Update: update
Delete: destroy
```

A user action fires a `GET` request for `/people/1`. Explain in detail each step
required for data to be returned to the client. (bullet points or ordered list)

```md
- The router recieves the `GET` request and determines the appropriate controller and action
- The people controller is told to execute the show action on id 1
- The people controller calls the people model and gives it the instructions to find and retrieve the person with id 1
- The people model accesses the database and sends the information it has found back to the controller
- The people controller recieves the information and converts it into json
- The people controller sends the newly created json back to the client
```

What is the command to generate a new rails-api app?

```bash
bin/rake db:nuke_pave
```

What is the command to start an instance of a rails server?

```bash
bin/rails server
```

What are the commands to drop, create, migrate and seed a database from the command
line? (5 bullet points)

```bash
- bin/rake db:drop
- bin/rake db:create
- bin/rake db:migrate
- bin/rake db:examples
- bin/rake db:seed
```

What is the command to scaffold a pet with a name and age attributes (hint:
Also think of the data types for each attribute)?

```bash
bin/rails generate scaffold pets name:string age:integer
```
