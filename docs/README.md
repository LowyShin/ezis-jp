# ezisオンラインマニュアル

## インストール

1. 自分のパソコンのOSとDBMSに適合したファイルをダウンロードしてください。
  * https://github.com/LowyShin/ezis-jp#%E3%83%80%E3%82%A6%E3%83%B3%E3%83%AD%E3%83%BC%E3%83%89
  * DBMSの詳細データを収集するので最低でも100GB以上の容量があるパソコンを推奨します。
  * パソコンは他の端末から接続できるネットワークにあるとWebブラウザーで複数のユーザーが接続・管理ができるのでその点を考慮して物理環境をお選び頂ければと思います。
  * ezisが実行されるとCPUとDiskのリソースがかなり消費するので作業用のPCよりは別途のPCを用意したほうを推奨します。
  * AWS上のVMなどを利用するのも方法ですが、スペックとデータのやり取りなどを考慮してオフィスに置く方法と視野に入れておくことを推奨します。
2. ダウンロードしたzipファイルを解凍します。
3. 解凍したフォルダーから「install.bat」を実行します。
4. 実行すると設定画面に移ります。
![install top](https://github.com/LowyShin/ezis-jp/blob/main/images/man/ezis-inst-01.png)
5. 使いたいDBポートとWebポートを指定して3を押下してエンターを押すとインストールされます。

## 初期設定

1. インストールファイルと同じフォルダーに生成されたmanage.batファイルを起動します。
2. 「1」を押してエンターキーを押下するとサービスが起動します。
  * 初期設定したDBポートとWebポートを既に他のプロセスが使っている場合サービスが起動できないので修正してから再起動してください。
3. サービスが正常に起動されたらWebブラウザーで接続してみます。
  * http://localhost:8080
4. 初期Web管理ツールのアカウントは下記になります。
  * User : admin
  * Password : admin
5. 最初ログインするとプロダクトキーを要求します。無料のキーをご提供致しますので営業担当にお問い合わせください。
6. プロダクトキーファイルを選択して「Verify」をクリックするとロックが解除され再度ログインが必要になります。
7. 再度ログインするとサーバーが登録されてないので登録メッセージが表示されます。
8. サーバー登録は「運用」メニューのサーバー登録をご参考ください。

## 運用

### サーバー登録

1. 「Setting」＞「Server」をクリックしてサーバー管理画面に移動します。
2. 「Add」をクリックして行を増やします。
3. サーバー管理に必要な情報を登録します。
  * ログインアカウントはDBMSの管理権限が必要なのでシステムが閲覧できる権限のアカウントをご入力ください。
4. 登録したサーバーの左にチェックボックスをクリックして接続テストを行います。
  * 正常に接続ができたら「ok」が表示されますが、表示されなかった場合はアカウント・ポートなどをご確認ください。
  * Firewall・ACL・セキュリティグループなどの設定で接続できない状況には各担当者にお問い合わせください。
5. 登録が完了すると右上のアラートにサービス再起動メッセージが表示されます。
6. 表示されたサービス再起動メッセージをクリックすると再起動されます。
  * サービス再起動はDBMSには影響がありません。
  * 「サービス再起動が失敗」とメッセージが表示されても内部的には再起動しているのでしばらくお待ち頂ければ正常に情報が見れます。



## 機能の見方

### Activity

* Activity(ORACLE)
  * Active Sessions Count
  * redo size
  * Execute to Parse % 
  * enqueue waits
  * logons current
  * user commits
  * session logical reads
  * physical blocks read
  * Memory Usage %
  * TOP physical blocks read
  * TOP Active Sessions Count
  * ActiveSessions Elapsed Time
  * Session
    * Active Only
    * Auto Refresh
    * Manual Refresh
  * Lock
  * Event

* Activity(MySQL, Mariadb)
  * Connections
  * Questions
  * Threads_connected
  * Threads_running
  * Bytes_sent
  * Bytes_received
  * Innodb_row_lock_waits
  * Aborted_connects
  * Aborted_clients
  * TOP Com_select
  * TOP Com_update
  * ActiveSessions Elapsed Time
  * Threads
    * Execlude sleep
  * Lock
  * Event

* Activity(SQL Server)
  * Active Sessions Count
  * Lock Count
  * Total Wait Time (ms)
  * Page reads/sec
  * Page writes/sec
  * User Connections
  * Buffer Cache Hit %
  * Average Latch Wait Time
  * TOP Active Sessions Count
  * TOP Total Wait Time (ms)
  * ActiveSessions Elapsed Time
  * Session
    * Execlude sleep
  * Lock
  * Event

* Session



### Performance

* Server
  * 見たいサーバーをクリックするとそのサーバーの性能情報に切り替わります。初期値は最初のサーバーになるのでご注意ください。
* Time Line
  * 好きな時間帯にマウスをドラッグするとその時間帯の状態が確認できます。（最短1時間単位）
* Top Activity
* TopSql
  * Actifity
  * Disk Reads
  * Elapsed
  * CPU Time
  * P/Reads(Physical Reads)
  * L/Reads(Logical Reads)
  * Buffer Gets
  * Block Changes
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
* Services
* Throughput
  * per second
  * transactions
* Active Session
* Lock

### LockWait(MySQL, Mariadb)

### WaitAnalysis(ORACLE, SQL Server)

### EventAnalysis(ORACLE, SQL Server)

### SQLAnalysis(ORACLE)

### ChangeTracking(ORACLE)

### CapacityManagement

### TraceFile(ORACLE)

### Setting




