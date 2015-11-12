
## Params

* ホワイトリスト処理は `params`メソッドで行う

```ruby
# apps/web/controllers/signup/create.rb
module Web::Controllers::Signup
  class Create
    include Web::Action

    params do
      param :email
      param :password

      param :address do
        param :country
      end
    end

    def call(params)
      puts params[:email]             # => "alice@example.org"
      puts params[:password]          # => "secret"
      puts params[:address][:country] # => "Italy"
      puts params[:admin]             # => nil
    end
  end
end
```
