## WaitAnalysis

* DBMS選択
* Timeline
* Wait Analysis
    * Event
    * Class
    * Exclude Background
        * チェックを入れるとバックグラウンド処理は除外されます。
    * Active
        * チェックを入れると休止状態のSQLは表示されません。
    * Graph
        * SQL*Net message from client
        * SQL*Net message to client
        * log file sync
        * [enq: TX - row lock contention](dics.md#enq-tx---row-lock-contention)
        * SQL*Net more data from client
        * db file sequential read
        * Disk file operations I/O
        * buffer busy waits
        * latch:cache buffers chains
        * [enq: TX - index contention](dics.md#enq-tx---index-contention)
        * enq: SQ - contention
        * latch: enqueue hash chains
        * read by other session
        * SQL*Net message from dblink
        * library cache: mutex X
        * latch:redo allocation
        * direct path read
        * latch:cache buffers lru chain
        * latch free
* Wait SQL
    * Time
    * sid
        * クリックすると[セッション詳細](#セッション詳細session-detail)が表示されます。
    * serial
    * username
    * module
    * sql_id
    * sql_fulltext
    * event
    * wait_class
    * wait_time
    * seconds_in_wait
    * cpu
    * redosize
    * L/Reads
    * P/Reads
    * executions
* Session
* Lock Tree
* Transaction

### セッション詳細(Session Detail)

* Session Tracking
    * CPU
    * Exec Count
    * Enq Waits 
    * Logons Current
    * P/Reads
    * L/Reads
    * Redo
* Session
    * session
        * sid
        * serial
        * status
        * type
        * sql_id
        * username
        * sql_exec_start
        * last_call_et
        * program
        * module
        * machine
        * port
        * ecid
        * state
        * sql_address
        * saddr
        * paddr
    * wait
        * event
        * wait_class
        * blocking_session
        * blocking_session_status
    * value
        * executecount
        * physicalreads
        * enqueuewaits
        * logonscurrent
        * sessionlogicalreads
        * redosize
        * undchangevectorsize
        * consistent_changes
        * block_changes
* Sql History
    * Time
    * sid
    * serial
    * status
    * type
    * sql_id
        * クリックすると[SQL詳細](func-performance-oracle.md#sql-detailsql詳細)画面が開きます。
    * username
        * SQL実行のためにDBMSにログインしたユーザー
    * sql_exec_start
    * LC/ET
    * wait_class
* Open_cursor
    * Time
    * sql_id
    * sql_text
    * user_name
    * Cursor_type
    * CNT
    * last_sql_active_time
* Process
    * Time
    * pid
    * spid
    * username
    * serial
    * termial
    * program
    * traceid
    * background
    * latchwait
    * latchspin
    * pga_used_mem
    * pga_alloc_mem
    * pga_freeable
    * pga_max_mem
* I/O
    * Time
    * sid
    * block_gets
    * consistent_gets
    * physical_reads
    * block_changes
    * consistent_changes
    * optimized_physical_reads
* Lock
    * tree
    * sid
    * sql_id
    * blocking_session
    * object_id
    * serial
    * username
    * machine
    * terminal
    * program
* PQ
    * saddr
    * sid
    * serial
    * audsid
    * paddr
    * username
    * command
    * ownerid
    * taddr
* Access
    * Time
    * sid
    * object
    * owner
    * type
* Transaction
    * Time
    * Transaction_Name
    * Transaction_start
    * Transaction_Age
    * UndoRecordsUsed
    * UndoBlocksUsed
    * Transaction_Status
* Log ops
    * sid
    * complete
    * message
    * start_time
    * elapsed_seconds
    * context
    * time_remaining
* Sql text
    * Format SQL
    * Auto Bind
    * Copy
* Plan
    * id
    * operation
    * name
    * optimizer
* Sql info
    * 選択した日の全体統計データ
    * first_load_time
    * disk_reads
    * user_io_wait_time
    * elapsed_time
    * sorts
    * optimizer_mode
    * last_active_time
    * buffer_gets
    * cpu_time
    * executions
    * version_count
    * plan_hash_value

