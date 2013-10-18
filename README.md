__Caution : Still under developpement and subject to changes__ 
# LemonWay

Ruby API client to query LemonWay web merchant and blank label APIs

Documentation at http://rubydoc.info/github/Paymium/lemon_way

## Installation

Add this line to your application's Gemfile:

    gem 'lemon_way'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install lemon_way

## Usage

```ruby
LemonWay::Client::WhiteLabel.init   base_uri: "https://ws.lemonway.fr/mb/test/dev/directkit/service.asmx",
                                    wl_login: "test",
                                    wl_pass: "test",
                                    wl_PDV: "test",
                                    language: "fr",
                                    version: "1.0",
                                    channel: "W",
                                    wallet_ip: "1.1.1.1"                                   

register_wallet_params =          { wallet: "123456789", 
                                    client_mail: "test@test.com", 
                                    client_title: "M", 
                                    client_first_name: "Martin", 
                                    client_last_name: "Dupont" 
                                  }

LemonWay::Client::WhiteLabel.register_wallet register_wallet_params
```

See [this page](http://rubydoc.info/github/Paymium/lemon_way/LemonWay/Client/WhiteLabel) for details.


## Todo

1. Complete the doc
2. Test with VCR
3. Build WebMerchant client


## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
