# admichat

A simple web chat for talking web admin

## Prerequisite

* Rust and Cargo
* Ruby 2.4+
* sh

## How to run

### static file

````
ruby -run -ehttpd . -p10001
````

### websocket

In another window:
````
cargo run
````

### message processing server

For example:
````ruby
require 'sinatra'

post '/mod_msg' do
  request.body.rewind
  puts request.body.read
  "!!!"
end
````

Run it at localhost:4567

## URL

* http://localhost:10001/chat-guest.html, for client/guest/customer
* http://localhost:10001/chat-admin.html, for admin


## TODO

* SSL
* Admin page should require authentication