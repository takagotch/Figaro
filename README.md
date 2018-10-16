### Figaro
---

https://github.com/laserlemon/figaro

```
gem 'figaro'
bundle exec figaro install

heroku config:set google_analytics_key=UA-35722661-5
figaro heroku:set -e production
figaro help heroku:set
figaro heroku:set -e production
figaro help heroku:set

```

```ruby
# config/application.yml
pusher_app_id: "2954"
pusher_key: "xxxxxxxxxxx"
pusher_secret: "xxxxxxxxxxxx"

# config/initializers/pusher.rb
Pusher.app_id = ENV["pusher_app_id"]
Pusher.key = ENV["pusher_key"]
Pusher.secret = ENV["pusher_secret"]

ENV["stripe_api_key"]
ENV.key?["stripe_api_key"]
ENV["google_analytics_key"]
ENV.key?("google_analytics_key")
Figaro.env.stripe_api_key
Figaro.env.stripe_api_key?
Figaro.env.google_analytics_key
Figaro.env.google_analytics_key?

# config/initializers/figaro.rb
Figaro.require_keys("pusher_app_id", "pusher_key", "pusher_secret")

# config/initializers/pusher.rb
Pusher.app_id = Figaro.env.pusher_app_id!
Pusher.key = Figaro.env.pusher_key!
Pusher.secret = Figaro.env.pusher_secret!

# config/spring.rb
%w(
   ...
   config/application.yml
).each { |path| Spring.watch(path) }

```
```
# config/application.yml
pusher_app_id: "2954"
pusher_key: "xxxxxxxx"
pusher_secret: "xxxxxxxxx"
test:
  pusher_app_id: "5112"
  pusher_key: "xxxxxxxxxx"
  pusher_secret: "xxxxxxxxxx"
  
# config/application.yml
google_analytics_key: "UA-35722661"
text:
  google_analytics_key: ~
  
# config/application.yml
stripe_api_key: "sk_live_xxxxxxxxxxx"
  
```

```
```

