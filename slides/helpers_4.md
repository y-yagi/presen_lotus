
## Formの例

生成されるHTMLは下記の通り

```html
<!doctype HTML>
<html>
  <head>
    <title>BookLayout</title>
  </head>
  <body>
    <h1>Bookshelf</h1>
    <h2>Add book</h2>
    <form action="/books" method="POST" accept-charset="utf-8" id="book-form">
      <input type="hidden" name="_csrf_token" value="926b70d777aeee0c47e98769be0116ff583f2d11ec90fdee6056cb44eccd4af2">
      <div class="input">
        <label for="book-name">Name</label>
        <input type="text" name="book[name]" id="book-name" value="">
      </div>
      <div class="controls">
        <button type="submit">Create Book</button>
      </div>
    </form>
  </body>
</html>
```
CSRFトークンも生成される
