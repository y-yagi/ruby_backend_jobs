### [Sidekiq](https://github.com/mperham/sidekiq)

* バックエンドはRedis.
* Resqueと互換性がある. Resqueのマルチスレッド版みたいな感じ(Resqueはマルチプロセス) . マルチスレッドなので、Resqueよりも比べてリソースの消費は少ない. ただ、ジョブをスレッドセーフにする必要あり.
* admin interfaceをデフォルトで搭載.
* 有料[Pro版](http://sidekiq.org/pro/)がある. $750.00/year...
