## Performance

* Server
  * 見たいサーバーをクリックするとそのサーバーの性能情報に切り替わります。初期値は最初のサーバーになるのでご注意ください。
* Time Line
  * 好きな時間帯にマウスをドラッグするとその時間帯の状態が確認できます。（最短1時間単位）
* Top Activity
* TopSql
  * Types
    * Activity
    * Disk Reads
    * Elapsed
    * CPU Time
    * P/Reads(Physical Reads)
    * L/Reads(Logical Reads)
    * Buffer Gets
    * Block Changes
  * sql_id
    * 実行したSQL IDを表示
    * クリックすると[SQLの詳細画面](#sql-detailsql詳細)が開きます。
* TopSession
  * CPU Used
  * Execute count
  * L/Reads
  * P/Reads
  * Redo
* Sysstat
  * % Non-Parse CPU
  * Active Sessions Count
  * Block Changes
  * Buffer Hit %
  * Buffer Nowait %
  * consistent changes
  * CPU used by this session
  * Data Dictionary Hit Ratio
  * db block changes
  * enqueue waits
  * execute count
  * Execute to Parse %
  * In-memory Sort %
  * Latch Hit %
  * Library Cache Get Hit %
  * Library Cache Pin Hit %
  * Lock Count
  * logons cumulative
  * logons current
  * Memory Usage %
  * Parse CPU to Parse Elapsed %
  * physical blocks read
  * Redo Nowait %
  * redo size
  * session logical reads
  * SessionEvent/db file scattered read
  * SessionEvent/Enq
  * SessionEvent/library cache pin
  * SessionEvent/log file sync
  * Soft Parse %
  * Total Wait
  * undo change vector size
  * user commits
  * user rollbacks
* IO
  * IO Type
    * Read Req
    * Write Req
    * Read MB
    * Write MB
  * IO Function
    * Others(MB)
    * Others(Req)
    * XDB(MB)
    * XDB(Req)
    * Streams AQ(MB)
    * Streams AQ(Req)
    * Smart Scan(MB)
    * Smart Scan(Req)
    * Direct Reads(MB)
    * Direct Reads(Req)
    * DBWR(MB)
    * DBWR(Req)
    * Data Pump(MB)
    * Data Pump(Req)
    * Direct Writes(MB)
    * Direct Writes(Req)
    * Recovery(MB)
    * Recovery(Req)
    * RMAN(MB)
    * RMAN(Req)
    * ARCH(MB)
    * ARCH(Req)
    * Archive Manager(MB)
    * Archive Manager(Req)
    * LGWR(MB)
    * LGWR(Req)
    * Buffer Cache Reads(MB)
    * Buffer Cache Reads(Req)
* Parallel Execution
  * Active Serial Session
  * Active Parallel Sessions
  * PQ QC Session Count
  * PQ Slave Session Count
  * DDL statements parallelized Per Sec
  * DML statements parallelized Per Sec
  * Queries parallelized Per Sec
* Services
  * Background Checkpoints Per Sec
  * Background CPU Usage Per Sec
  * Background Time Per Sec
* Throughput
  * per second
  * transactions
* Active Session
  * value_avg
  * value_max
* Lock
* Latency

### SQL Detail(SQL詳細)
* Sql text
  * Format SQL
    * SQLを見やすく自動的に行分けをしてくれます。
  * Copy
* Sql text(bind)
* Bind
* SQL Tracking
  * disk reads
  * buffer gets
  * user IO wait time
  * cpu time
  * elapsedtime
  * executions
* SQL Find
* 日付指定
* SQL info
  * 選択した日付の1日処理した統計情報です。Performanceメニューから1時間等期間を縮めてもこのデータは変わりません。
  * first_load_time
  * disk_reads
  * user_io_wait_time
  * ElapsedTime(ms) AVG
  * sorts
  * optimizer_mode
  * module
  * last active_time
  * buffer_gets
  * cpu_time
  * executions
  * version_count
  * plan_hash_value
* Plan
  * 「Sql text(bind)」メニューから一回プランを作ると削除されるまで表示されます。
* Plan History
  * Planを作成した履歴を表示されます。

