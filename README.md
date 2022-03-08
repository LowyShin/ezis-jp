# データベースのインサイトを探る！

## Problem

今までのデータベースの監視は普通のモニタリングツールでしか利用できなかったと思います。

障害が起きてもその瞬間を逃したらサーバーの状況しか確認できず

DBの問題だとしても把握できてないのが現実でした。

問題があったとしてもログを見たりSlow Queryを残して目視で見ながら推測するしかないのが現実です。


## Solution

障害が起きた後でも時点を遡って問題があった時のSQLから影響を追跡ができます！

同じタイミングで実行されたSQLを全て見ることができます。

実際に時間がかかったSQLを見ると問題がないケースが多いのはChain Lockの影響で実際の問題SQLは時間内で処理されて後の正常なSQLだけ残ったからです。

このChain Lockの原因を見つけることができるツールです！


## 特徴

* Agent方式ではない
  * 物理サーバーだけではなくAWS RDS・Azure SQLなどのサービス型DBMSもDBMS性能が把握できます。
* DBの性能監視
  * DBMSが自分の性能を測定するために収集したデータから監視するので負荷ではなく「性能」をモニタリングしています。
* タイムマシン機能
  * 問題が起きた時点のDBの状況が詳しく確認できます。
  * 過去のデータを探すためにログファイルを探したりメモリ上のデータを見たりモニタリングツールを見たりする手間が省けます。

![Session-SQL-Analysis](https://github.com/LowyShin/ezis-jp/blob/main/images/intro/ezis-intro-session-sqlana.png)

* 横展開可能なUI
  * 問題が起きた時点を基準に調査しながら並列の調査がしやすくリンクをサポートしてます。
* 性能測定に必要な機能
  * 抽出したSQLからQuery Planをリアルタイムで分析し性能の問題などが分かります。
  * 実行回数・CPU占有率などをSQLごとに確認してSQL自体の問題を把握できます。
* 遅延の原因を見つけるWait Analysis
  * 遅延する根本原因が分かる待機分析が強いです。
* Alert/ErrorなどのRDBMSのイベントを分析
  * 一般モニタリングツールではないDBMSのアラートを分析してリスクを表示します。
* データのパターンを見つけるChange Tracking(ORACLE)
  * データ・プランの変更管理が一目で把握できるので容量設計などの高いスキルが必要な設計も可能になります。
* 容量設計の基本データを確認するCapacity Management
  * ORACLEの場合実際容量とTable Spaceの容量が違うのでテーブルスペースが足りなくて障害が起きた経験が多いと思います。
  * 現在仕様可能なテーブルスペースの取得ができるので容量把握のためにサーバーに接続する必要がありません。
  * バックアップ管理・障害復旧の管理など容量設計に必要な情報を提供しています。
* ORACLEの場合AWR/ASH Reportが取れるまで待たないといけないですが、ezisはリアルタイムで性能の確認ができます。

## 手頃な価格

* MySQL(32GB以下メモリ)の場合だった2千円（月）！

### 価格表

* MySQL(Maria)
  * 2千円/月～
* PostgreSQL
  * 2千円/月～
* Oracle
  * 2万円/月～
* SQL Server
  * 1万円/月～
* オプション
  * 性能分析提案サービス
    * 98,000円/月

## 対応DBMS

* ORACLE
* SQL Server
* MySQL/MariaDB
* PostgreSQL

## 監視端末の推奨マシンスペック

* CPU : core i5級以上
* RAM : 8GB以上
* HDD : 100GB以上
  * ORACLEの場合インスタンスと負荷によって1日5GB以上残る場合もあるので負荷を見ながら計算が必要です。
  * MySQLの場合は1日500MBを目安として計算しています。
  * 設定画面でログの削除期間を設定できます。

## ダウンロード

ezisはサーバー側のAgentは不要なのでモニターする側のサーバーまたはパソコンにインストールする必要があります。

インストールしたらWebサーバーが立ち上がるので他の運用メンバーがインストールした端末にURLまたはIPで接続すると複数の人が管理できます。

### Windows

* [Ezis for ORACLE](https://www.ezis.cloud/downloads/ezis/oracle/windows)
* [Ezis for MySQL(Mariadb)](https://www.ezis.cloud/downloads/ezis/maria/windows)
* [Ezis for SQL Server](https://www.ezis.cloud/downloads/ezis/sqlserver/windows)
* [Ezis for PostgreSQL](https://www.ezis.cloud/downloads/ezis/postgre/windows)

### Ubuntu

* [Ezis for ORACLE](https://www.ezis.cloud/downloads/ezis/oracle/linux)
* [Ezis for MySQL(Mariadb)](https://www.ezis.cloud/downloads/ezis/maria/linux)
* [Ezis for SQL Server](https://www.ezis.cloud/downloads/ezis/sqlserver/linux)
* [Ezis for PostgreSQL](https://www.ezis.cloud/downloads/ezis/postgre/linux)

## お問い合わせ

lowyshin@shinsema.jp

## リンク

* [全てのRPAツールを統合管理！giip RPA orchestrator](https://giipasp.azurewebsites.net)
