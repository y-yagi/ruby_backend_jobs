### [Delayed Job](https://github.com/collectiveidea/delayed_job)

* バックエンドは基本はDB. ただ、MongoDBでも使える(delayed_job_mongoid).
* ActiveRecord前提
* 昔は名前付きキューとか使えなかったけど、今は使えるようになったりと色々改善している
  * エラー時のコールバック処理が指定出来るようになると嬉しいのだが…
