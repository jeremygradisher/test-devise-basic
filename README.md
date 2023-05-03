# Test Devise basic set-up with Rails 7

Reference: https://www.digitalocean.com/community/tutorials/how-to-set-up-user-authentication-with-devise-in-a-rails-7-application

## Initial setup:

1. Create a new app:
```
rails new test-devise-basic --css=bootstrap --javascript=esbuild --database=postgresql
```

2. bundle install
```
bundle install
```

3. type the bin/setup command to install the dependencies and create the database:
```
bin/setup
```

4. We can now run the rails server, and the scripts that precompile the CSS and the JavaScript code with the bin/dev command:
```
bin/dev
```

5. We can now go to http://localhost:3000, and we should see the Rails boot screen.

6. If you cloned this, Precompile javascript/css: ```rails assets:precompile```

## Create a landing page:

7. Create a new controller named "home" by running the following command in your terminal:
```
rails generate controller Home index
```

8. Open the config/routes.rb file and add the following line:
```
root 'home#index'
or
get '/home', to: 'home#index'
```
## Installing and Configuring Devise

9. add Devise gem:
```
gem "devise"
```

10. bundle install
```
bundle install
```

11. All the Devise gem to generate your assets:
```
bin/rails g devise:install
```
That got you this:<br>
* create  config/initializers/devise.rb
* create  config/locales/devise.en.yml

12. Open config/initializers/devise.rb for editing - This line adds turbo_stream as a navigational format. You need to add this for Devise 4.8.1 to work with Rails 7; otherwise, you’d get an undefined method user_url error.
```
Devise.setup do |config|
  # ...

  config.navigational_formats = ['*/*', :html, :turbo_stream]

  # ...
end
```

13. make sure we have the flash message stuff in app/views/layouts/application.html.erb:
```
<body>
  <p class="notice"><%= notice %></p> 
  <p class="alert"><%= alert %></p> 
  <%= yield %>
</body>
```

## Creating the User Model with Devise

14. 











