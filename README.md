# Devise-JWT with a CRUD Example

A Ruby on Rails API with a CRUD using Devise-JWT to login/register. 

### Before starting

I recommend you to follow the link first 2 tutorials recommended bellow in the links to understand this project.

### Prerequisites

Before starting you need some background on Ruby and Rails. Check the links bellow.

You need a working environment with Ruby on Rails installed and PostgreSQL as well.

### Installing

Open a command line console and clone this project.

```
git clone https://github.com/tcrurav/Devise-JWT-Bicycles
```

Go to the new created directory

```
cd Devise-JWT-Bicycles
```

Install all dependencies

```
bundle install
```

Now generate a secret key. And note the output. We’ll add this into our credentials file momentarily.

```
rake secret
```

Generate rails credentials. The commands below will create the config/master.key and config/credentials.yml.enc files:

```
SET EDITOR="C:\Windows\System32\notepad.exe"
rails credentials:edit
```

The notepad will open up. Now paste in the following, with the key generated from running rake secret above.

```
devise:
  jwt_secret_key: <rake secret key>
```

Change the file config/database.yml

```
database: ruby_bicycles_development
username: postgres  
password: <your password>
```

Now make all migrations:

```
rails db:create db:migrate
```

Now the seeds:

```
rails db:seed
```

Boot your API

```
rails s
```

Now it's time to enjoy this project. Test your API with POSTMAN using the following requests:
https://documenter.getpostman.com/view/3446841/UVeNkMk2


The recommended order for the POSTMAN requests will be:

```
GET http://localhost:3000/bicycles
```

You'll get a message saying 'You are not logged in'.

Now register a user and log in:

```
Post http://localhost:3000/users
POST http://localhost:3000/users/sign_in
```

Copy the Bearer Token in the headers returned, and use it in the following request:

```
GET http://localhost:3000/bicycles
```

Now you'll get the info. Congrats!!!

Try the other resquests as well...


## Built With

* [Rails](https://rubyonrails.org/) - Rails is a full-stack framework. It ships with all the tools needed to build amazing web apps on both the front and back end
* [devise-jwt](https://rubygems.org/gems/devise-jwt/versions/0.5.6?locale=es) - JWT authentication for devise with configurable token revocation strategies.
* [PostgreSQL](https://www.postgresql.org/) - The World's Most Advanced Open Source Relational Database


## Acknowledgments

* https://medium.com/ruby-daily/a-devise-jwt-tutorial-for-authenticating-users-in-ruby-on-rails-ca214898318e. A Devise-JWT Tutorial For Authenticating Users in Ruby on Rails.
* https://dev.to/lisahjung/beginner-s-guide-to-creating-an-api-from-scratch-using-rails-2eie. Beginner's guide to creating an API from scratch using Rails.
* https://guides.rubyonrails.org/v5.0/getting_started.html. Getting Started with Rails.
* https://stackoverflow.com/questions/57402435/how-to-run-rails-credentialsedit-on-windows-10-without-installing-a-linux-sub. How to run 'rails credentials:edit' on Windows 10.
* https://gist.github.com/db0sch/19c321cbc727917bc0e12849a7565af9. Regenerate Rails credentials.
