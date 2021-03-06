# RCredStash [![Build Status](https://travis-ci.org/adorechic/rcredstash.svg?branch=master)](https://travis-ci.org/adorechic/rcredstash)

RCredStash is a ruby port of [CredStash](https://github.com/fugue/credstash)


## Installation

Add this line to your application's Gemfile:

```ruby
gem 'rcredstash'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install rcredstash

## Usage

```ruby
CredStash.get(key)
CredStash.put(key, value)
CredStash.list
CredStash.delete(key)
```

### AWS credentials
RCredStash uses [aws-sdk v2](https://github.com/aws/aws-sdk-ruby), so configuration options provided by aws-sdk such as `ENV['AWS_ACCESS_KEY_ID']` and `ENV['AWS_SECRET_ACCESS_KEY']` are available.

### Configurations

```ruby
CredStash.configure do |config|
  config.table_name = 'your_dynamodb_table_name'
end
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/adorechic/rcredstash.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
