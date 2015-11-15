
## Repositories

* Railsで言う`scope`的な
* `query`メソッドは`Lotus::Model::Adapters::Sql::Query`クラスを返し、メソッドチェーンが出来る

```ruby
BookRepository.most_recent_by_author(author).order_by_price
```
