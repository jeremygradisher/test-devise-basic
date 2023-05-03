# Test Devise basic set-up with Rails 7

Reference: https://www.digitalocean.com/community/tutorials/how-to-set-up-user-authentication-with-devise-in-a-rails-7-application

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

7. 