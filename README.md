# GraphqlPlayground::Rails
A blatant copy of [GraphiQL::Rails](https://github.com/rmosolgo/graphiql-rails) with much less functionality but with [GraphQL Playground](https://github.com/graphcool/graphql-playground) instead.

## Installation
Add this line to your application's Gemfile:

```ruby
gem 'graphql_playground-rails'
```

And then execute:
```bash
$ bundle
```

Or install it yourself as:
```bash
$ gem install graphql_playground-rails
```

### Mount the Engine

Add the engine to `routes.rb`:

```ruby
# config/routes.rb
Rails.application.routes.draw do
  # ...
  if Rails.env.development?
    mount GraphqlPlayground::Rails::Engine, at: "/graphiql", graphql_path: "/your/endpoint"
  end
end
```

## Contributing
Contribution directions go here.

## License
The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
