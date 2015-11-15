
## Repositories

* RDBMSのORMには[jeremyevans/sequel](https://github.com/jeremyevans/sequel)を使用
* クエリーを書く用の、`query`メソッドがある
```
class BookRepository
  include Lotus::Repository
  def self.most_recent_by_author(author, limit: 8)
    query do
      where(author_id: author.id).limit(limit)
    end
  end

  def self.order_by_price
    query { order(:price) }
  end
end
```
