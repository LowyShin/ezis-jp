# Performance - ezis DB パフォーマンス分析ツール

* DBMS選択
* Time Line
* Statement
    * [Questions](dics.md#questions)
    * [Com_select](dics.md#comselect)
    * [Com_insert](dics.md#cominsert)
    * [Com_update](dics.md#comupdate)
    * [Com_delete](dics.md#comdelete)
* Queries
    * [Time](dics.md#time)
    * [sqltext](dics.md#sqltext)
    * [count](dics.md#count)
    * [db](dics.md#db)
    * [avg_elapsed_time_sec](dics.md#avgelapsedtimesec)
    * [max_elapsed_time_sec](dics.md#maxelapsedtimesec)
* Threads Running
    * [Exlcude sleep](dics.md#exlcude-sleep)
    * [Time](dics.md#time)
    * id
    * [thread_id](dics.md#threadid)
    * [sqltext](dics.md#sqltext)
    * [user](dics.md#user)
    * [host](dics.md#host)
    * [db](dics.md#db)
    * [command](dics.md)
    * [elapsed time(ms)](dics.md#elapsed-timems)
    * [wait time(ms)](dics.md#wait-timems)
    * [state](dics.md#state)
    * [processlist_state](dics.md#processliststate)
* Statements Summary
    * [Time](dics.md#time)
    * [sqltext](dics.md#sqltext)
    * [schema_name](dics.md#schemaname)
    * [fullscan](dics.md#fullscan)
    * [exec_count](dics.md#execcount)
    * [err_count](dics.md#errcount)
    * [exec_time_total_ms](dics.md#exectimetotalms)
    * [exec_time_max_ms](dics.md#exectimemaxms)
    * [exec_time_avg_ms](dics.md#exectimeavgms)
    * [sum_rows_sent](dics.md#sumrowssent)
    * rows_sent_avg
    * rows_scanned
* Sysstat
    * Aborted_clients
    * Aborted_connects
    * Binlog_cache_disk_use
    * Binlog_cache_use
    * Binlog_stmt_cache_disk_use
    * Binlog_stmt_cache_use
    * Bytes_received
    * Bytes_sent
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
    * Connections
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
    * Key_write_requests
    * Key_writes
    * Lock count
    * Max_used_connections
    * OCom_delete_multi
    * Qcache_queries_in_cache
    * Questions
    * Slave_connections
    * Sort_rows
    * Sort_scan
    * Threads count
    * Threads_connected
* Connections
    * Threads_connected
    * Max_used_connections
    * Slave_connections
    * Connection_errors_internal
    * Aborted_connects
    * Connection_errors_max_connections
* Thread Activity
    * Threads_running(AVG)
    * Threads_running(MAX)
    * Threads_connected
* Query Throughtput
    * Questions
    * Com_select
    * Write

