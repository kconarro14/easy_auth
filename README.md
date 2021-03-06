# EasyAuth

An easy(ish) way to use API tokens in your services

## Installation

Add this line to your application's Gemfile:

    gem 'ez_auth', :require => "easy_auth"

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install ez_auth

## Usage

Set your API token for your service:

    $ export API_TOKEN=your_api_token

Include in your controller

```ruby
class ApplicationController < ActionController::Base
  include EasyAuth
  before_filter :easy_authenticate!
end
```

Add your API token to your request header on your client:

    $ curl --header "X-API-TOKEN: your_api_token" api.yourservice.com

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
