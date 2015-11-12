
## Models

* `book`というエンティティがあった場合

```ruby
# lib/bookshelf/entities/book.rb(エンティティ)
class Book
  include Lotus::Entity
  attributes :name, :price, :code, :author_id

  def author
    AuthorRepository.find(author_id)
  end
end
```

```ruby
# lib/bookshelf/repositories/book_repository.rb(リポジトリ)
class BookRepository
  include Lotus::Repository
end
```
