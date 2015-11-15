
## Params

* `param`に直接validationも書けたりもする

```ruby
# apps/web/controllers/signup/create.rb
module Web::Controllers::Signup
  class Create
    include Web::Action
    MEGABYTE = 1024 ** 2

    params do
      param :name,             presence: true
      param :email,            presence: true, format: /@/, confirmation: true
      param :password,         presence: true,              confirmation: true
      param :terms_of_service, acceptance: true
      param :avatar,           size: 0..(MEGABYTE * 3)
      param :age,              type: Integer, size: 18..99
    end

    def call(params)
      if params.valid?
        # ...
      else
        # ...
      end
    end
  end
end
```
