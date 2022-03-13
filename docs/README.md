# ezisオンラインマニュアル

## 始めに

1. [インストール](install.md)

2. [初期設定](initialize.md)

## 運用

* [運用マニュアル](management.md)

### ORACLEの機能

  * [Activity(ORACLE)](func-activity-oracle.md)
    * 現在の状態を様々なデータで見れるダッシュボード
  * [Performance(ORACLE)](func-performance-oracle.md)
    * 過去の時間に戻ってパフォーマンスが詳しく分析できる機能
  * [WaitAnalysis(ORACLE)](func-waitanalysis-oracle.md)
    * 待機分析で遅れの根本原因を分析する機能
  * [EventAnalysis(ORACLE)](func-eventanalysis-oracle.md)
    * DBMSのイベントメッセージを分析する機能
  * [SQLAnalysis(ORACLE)](func-sqlanalysis-oracle.md)
    * SQL毎の詳細分析をする機能
  * [ChangeTracking(ORACLE)](func-changetracking-oracle.md)
    * データ・テーブル仕様の変更などで急にパフォーマンス低下が発生した場合詳細がわかる機能
  * [CapacityManagement(ORACLE)](func-capacitymanagement-oracle.md)
    * データサイズの変化を詳しく分析しデータの蓄積の仕方によるパフォーマンス低下の原因を見つけることができる
    * 毎日のデータ量の変化がグラフで見える
    * テーブル毎・テーブルスペースなどデータ量を詳細に見れるのでIO分散計画の元データが抽出できる。
    * AWS RDS/Azure SQLなどのクラウドデータベースサービスの場合にも現在使っている容量が把握できるので容量計画に必要な情報が取れる
  * [TraceFile(ORACLE)](func-tracefile-oracle.md)
    * ORACLEのTraceファイルをダウンロードができる

### MySQL/Mariadbの機能

  * [Activity(MySQL/Mariadb)](func-activity-mysql.md)
    * 現在の状態を様々なデータで見れるダッシュボード
  * [Threads(MySQL/Mariadb)](func-activity-mysql.md#テーブル式データ)
    * show processlistと同じデータが見れるメニュー
  * [Performance(MySQL/Mariadb)](func-performance-mysql.md)
    * 過去の時間に戻ってパフォーマンスが詳しく分析できる機能
  * [LockWait(MySQL/Mariadb)](func-lockwait-mysql.md)
    * Lock状態を分析してパフォーマンス低下の原因を探す
  * [EventAnalysis(MySQL/Mariadb)](func-eventanalysis-mysql.md)
    * DBMSのイベントメッセージを分析する機能
  * [CapacityManagement(MySQL/Mariadb)](func-capacitymanagement-mysql.md)
    * データサイズの変化を詳しく分析しデータの蓄積の仕方によるパフォーマンス低下の原因を見つけることができる
    * 毎日のデータ量の変化がグラフで見える
    * AWS RDS/Azure SQLなどのクラウドデータベースサービスの場合にも現在使っている容量が把握できるので容量計画に必要な情報が取れる


### SQL Serverの機能

  * Activity(SQL Server)
    * [Activity(SQL Server)](func-activity-sqlserver.md)
      * 現在の状態を様々なデータで見れるダッシュボード
    * [Session(SQL Server)](func-activity-sqlserver.md#session)
      * 現在接続したセッションが確認できる。
  * [Performance(SQL Server)](func-performance-sqlserver.md)
    * 過去の時間に戻ってパフォーマンスが詳しく分析できる機能
  * [WaitAnalysis(SQL Server)](func-waitanalysis-sqlserver.md)
    * 待機分析で遅れの根本原因を分析する機能
  * [EventAnalysis(SQL Server)](func-eventanalysis-sqlserver.md)
    * DBMSのイベントメッセージを分析する機能
  * [CapacityManagement(SQL Server)](func-capacitymanagement-sqlserver.md)
    * データサイズの変化を詳しく分析しデータの蓄積の仕方によるパフォーマンス低下の原因を見つけることができる
    * 毎日のデータ量の変化がグラフで見える
    * AWS RDS/Azure SQLなどのクラウドデータベースサービスの場合にも現在使っている容量が把握できるので容量計画に必要な情報が取れる

### PostgreSQLの機能

## Setting

### Users

* Users
  * ezisにログインするユーザーを管理します。
* [UserMgmt](setting-users-usermgmt.md)
* UserxAccount

### Monitoring

* Server
  * サーバー接続情報を登録すると監視が始まる。
* ServerMgmt
  * DBMSグループと接続を管理します。
* LoggingInfo
  * ezisのログに残している項目が確認できる。
* StatName

### Event

* SendMethod
* ProductEvent

### Advance

* [General](setting-advance-general.md)
* LoggingInfo
* [License](setting-advance-license.md)
  * ライセンスキーを入れてライセンスの変更ができる機能
