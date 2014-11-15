### [Que](https://github.com/chanks/que)

* PostgreSQL *だけ* で使えるjob client. PostgreSQLの[Advisory Locks](http://www.postgresql.org/docs/current/static/explicit-locking.html#ADVISORY-LOCKS)を使用している. (日本語のページは[こっち](https://www.postgresql.jp/document/9.1/html/explicit-locking.html#ADVISORY-LOCKS))
* 他のRDBMS-backendに比べて幾つかメリットがある
  * Concurrency: ワーカーは 他のjobのブロックを行わない. "SELECT FOR UPDATE"スタイルのロック処理を行う.
  * Efficiency: ロック処理はメモリで行われるので、diskへの書き込みは行われない. I/Oでボトルネックになる事はない.
  * Safety: Rubyのプロセスが死んでも、ジョブは失われず、直ぐに他のワーカーがピックアップして処理を行う
* RDMBSを使用しているキューの中では早い
  * [sample-output](https://github.com/chanks/queue-shootout#sample-output)
