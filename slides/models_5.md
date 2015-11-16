
## Adapters

* ストレージはRDBMS以外も使用出来るようになっている
* ストレージの指定は`adapter`で行う
* lotusが対応している`adapter`は以下
  * File System (default)
  * Memory
  * SQL
* デフォルトはファイルシステムになっているので、RDBMSを使わずにデータを保存/作成する、という事も可能
