# Devise-JWT with a CRUD Example

It's just that: a Ruby on Rails API with a CRUD. 

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

Change the file config/database.yml

```
password: <your password>
```

Follow the steps of the following link to generate rails credentials:
https://gist.github.com/db0sch/19c321cbc727917bc0e12849a7565af9

Install all dependencies

```
bundle install
```

Boot your API

```
rails s
```

Test your API with POSTMAN using the following requests:
https://documenter.getpostman.com/view/3446841/UVeNkMk2


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
