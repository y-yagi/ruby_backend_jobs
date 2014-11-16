## Active Jobが対応しているキューイングシステムの一覧

|                   | Async | Queues | Delayed   | Priorities | Timeout | Retries |
|-------------------|-------|--------|-----------|------------|---------|---------|
| Backburner        | Yes   | Yes    | Yes       | Yes        | Job     | Global  |
| Delayed Job       | Yes   | Yes    | Yes       | Job        | Global  | Global  |
| Qu                | Yes   | Yes    | No        | No         | No      | Global  |
| Que               | Yes   | Yes    | Yes       | Job        | No      | Job     |
| queue_classic     | Yes   | Yes    | No*       | No         | No      | No      |
| Resque            | Yes   | Yes    | Yes (Gem) | Queue      | Global  | Yes     |
| Sidekiq           | Yes   | Yes    | Yes       | Queue      | No      | Job     |
| Sneakers          | Yes   | Yes    | No        | Queue      | Queue   | No      |
| SuckerPunch       | Yes   | Yes    | No        | No         | No      | No      |


詳細は[Rails API guide](http://edgeapi.rubyonrails.org/classes/ActiveJob/QueueAdapters.html)参照
