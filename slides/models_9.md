
## Repositories

* `Lotus::Repository`では、下記メソッドが定義されている
  ```
  .persist(entity) – Create or update an entity
  .create(entity) – Create a record for the given entity
  .update(entity) – Update the record corresponding to the given entity
  .delete(entity) – Delete the record corresponding to the given entity
  .fetch(raw) – Fetch raw datasets for the given raw query string (eg. SQL)
  .execute(raw) – Execute raw command (eg. SQL)
  .all - Fetch all the entities from the collection
  .find - Fetch an entity from the collection by its ID
  .first - Fetch the first entity from the collection
  .last - Fetch the last entity from the collection
  .clear - Delete all the records from the collection
  .query - Fabricates a query object
  ```
* どのadapterを使用しても上記メソッドは使用可能
* SQL adapterではもうちょっとSQLラッパー用のメソッドが定義されている
