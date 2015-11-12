
## その他

* i18nはまだ無い
  * 対応自体は進められている [Error messages by jodosha · Pull Request #74 · lotus/validations](https://github.com/lotus/validations/pull/74)
  * 日本語…
* 環境固有の値はdotenvを使って設定するようになっている
```ruby
# .env.development
# Define ENV variables for development environment
BOOKSHELF_DATABASE_URL="postgres://localhost/bookshelf_development"
WEB_SESSIONS_SECRET="5c4b5645b0ccab42ad247bb9b9a98ea60135a000dd43f0d37eaa391389193773"
ADMIN_SESSIONS_SECRET="dbadab6c5844d67979b04a045a3caca7661b73fa5354ea7c36cc024f243966f2"
```
  * 上記ファイルがデフォルトで生成される

