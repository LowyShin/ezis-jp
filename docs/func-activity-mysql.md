# アクティビティ - ezis DB パフォーマンス分析ツール

* DBMS選択

### ezisお勧め

* ActiveSessions Elapsed Time
    * 現在処理しているセッションの数が点の大きさで、処理時間が高さで表示され一目で負荷が分かるグラフです。
* Top Com_select
* TOP Com_update

### グラフ

メイングラフから表示したい項目を9つ選択して調整ができます。

* Connections
* Questions
* THreads_connected
* Threads_running
* Bytes_sent
* Bytes_received
* Innodb_row_lock_waits
* Aborted_connects
* Aborted_clients
* Search
* Binlog_cache_disk_use
* Binlog_cache_use
* Binlog_stmt_cache_disk_use
* Binlog_stmt_cache_use
* Com_delete
* Com_insert
* Com_insert_select
* Com_load
* Com_replace
* Com_replace_select
* Com_select
* Com_update
* Com_update_multi
* Connection_errors_internal
* Connection_errors_max_connections
* Innodb_buffer_pool_pages_total
* Innodb_buffer_pool_read_rrequests
* Innodb_buffer_pool_reads
* Innodb_page_size
* Innodb_row_lock_current_waits
* Innodb_rows_updated
* Key_blocks_not_flushed
* Key_blocks_unused
* Key_blocks_used
* Key_read_requests
* Key_reads
* Lock count
* Max_used_connections
* OCom_delete_multi
* Qcache_queries_in_cache
* Slave_connections
* Sort_rows
* Sort_scan
* Threads count
* Threads_connected
* Threads_running

### テーブル式データ

* Threads
    * MySQLの`show processlist;`の出力結果を表示します。
    * Exclude sleep
        * 選択すると現在アクティブなSQLのみ表示されます。
    * ServerID
    * Time
    * id
    * thread_id
    * sqltest
    * user
    * host
    * db
    * command
    * elapsed_time_ms
    * wait_time_ms
    * state
    * processlist_state
    * memory_used_bytes
    * query_id
    * event_name
    * operation
    * trx_id
    * blocking_trx_id
    * lock_mode
    * trx_state
    * trx_started
* Lock
    * ServerID
    * Time
    * id
    * thread_id
    * sqltest
    * user
    * host
    * db
    * command
    * elapsed_time_ms
    * wait_time_ms
    * state
    * processlist_state
    * memory_used_bytes
    * query_id
    * event_name
    * operation
    * trx_id
    * blocking_trx_id
    * lock_mode
    * trx_state
    * trx_started


* Event

