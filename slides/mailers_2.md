
## Mailers

* 一つのメール毎に一つのメールクラスを定義する
  * Railsのように、一つのMailerクラス複数メソッドを定義は出来ない

```ruby
class Mailers::Welcome
  include Lotus::Mailer

  from    'noreply@bookshelf.org'
  to      'user@example.com'
  subject 'Welcome to Bookshelf'
end
```

```
Mailers::Welcome.deliver

Mailers::Welcome.deliver(format: :html)
Mailers::Welcome.deliver(format: :txt)
```
