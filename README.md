# BatchRequestClient

[![NetflixOSS Lifecycle](https://img.shields.io/osslifecycle/Netflix/osstracker.svg)]()

Ruby Client to create batch payload for use with [Batch Request API Middleware](https://github.com/Netflix/batch_request_api)

## Installation
Add this line to your application's Gemfile:

```ruby
gem 'batch_request_client'
```

Or install it yourself as:
```bash
$ gem install batch_request_client
```
## Usage

``` ruby
  BatchRequestApi::Client.create(payload, url)
  ```

## Arguments

* payload - Array of models.
* url - Complete route.

## Example:

``` ruby
  BatchRequestApi::Client.create(payload, 'http://localhost:3000/talents', :parallel)
```

Default is sequential operation, if you want parallel, you can pass ```:parallel``` in the list of arguments.

## Coming Soon

Update and Delete is still TODO, since we focussed on the [Ember Addon](https://github.com/Netflix/ember-batch-request) that handles update and delete from UI.

## Contributing
If you would like to contribute, you can fork the project, edit, and make a pull request.
