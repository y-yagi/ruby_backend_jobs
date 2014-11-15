### [Qu](https://github.com/bkeepers/qu)

* delayed_job、Resqueの不満点を解消しているらしい
  * delayed_job
    * 失敗した時何も通知がこない
    * 名前付きキューが使えなかった(これは昔の話かな)
    * 複数のワーカーを実行している際、時折違うワーカーで同じ処理が実行されてしまう事がある
  * Resque
    * Redisは良いバックエンドだけど、全ての環境でそうという訳ではない
    * Jobをフォークする前にメモリリークの予防をしなくてはならないが、沢山高速なジョブが実行されている環境では、これが訳に立たない([resque-jobs-per-fork](https://github.com/samgranieri/resque-jobs-per-fork)でちょっと対応出来る)

