### 個人的まとめ

* Redisを使える環境であれば、やっぱりsidekiq/resqueが良い気がする
  * どっちも必要そうな機能は一通り兼ね備えている
  * 個人的には、デフォルトでadmin画面を提供しているsidekiqがオススメ
* RDBMSしか使えないなら、やっぱりDelayed Jobが安定してそう
  * 性能を求めるならQue. ただ、PostgreSQL前提
