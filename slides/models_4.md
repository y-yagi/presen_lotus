
## Models

```
BookRepository.all
# => [#<Book:0x007f4dd7d3c4b8 @id=1, @name="aa", @price="100", @code="123", @author_id=1>, #<Book:0x007f4dd7d3c198 @id=2, @name="aaaa", @price="1", @code="ccc", @author_id=1>]
BookRepository.all.first
# => #<Book:0x007f4dd7d0ab48 @id=1, @name="aa", @price="100", @code="123", @author_id=1>

new_book = Book.new(name: "newbook", price: 1000, author_id: 1, code: '00077')
# => #<Book:0x007f4dd7bbdab0 @name="newbook", @price=1000, @code="00077", @author_id=1>
BookRepository.create(new_book)
# => #<Book:0x007f4dd7bb8f60 @id=5, @name="newbook", @price="1000", @code="00077", @author_id=1>
```
