
## Models

* `book`というエンティティがあった場合

```ruby
# lib/bookshelf/entities/book.rb
class Book
  include Lotus::Entity
  attributes :name, :price, :code, :author_id
end
```

```ruby
# lib/bookshelf/repositories/book_repository.rb
class BookRepository
  include Lotus::Repository
end
```
