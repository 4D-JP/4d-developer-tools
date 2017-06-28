# 4d-developer-tools
開発者向けのツール

**注記**: 各種ログファイルの仕様は[v16](http://doc.4d.com/4Dv16/4D/16.1/Appendix-E-Description-of-log-files.300-3373556.ja.html)で公開されました。

## Request Log Analyzer

[SET DATABASE PARAMETER](http://doc.4d.com/4Dv15/4D/15.4/SET-DATABASE-PARAMETER.301-3274410.ja.html)の``4D Server log recording (28)``および``Client Log Recording (45)``で出力したログファイルを解析するためのツール

### アーカイブ資料

[コマンドとリクエストの関係図](https://github.com/4D-JP/4d-developer-tools/blob/master/ReqLog.png)

[ニーモニック表（不完全）](https://github.com/4D-JP/4d-developer-tools/blob/master/RequestID.xls)

### Log Analyzer

[SET DATABASE PARAMETER](http://doc.4d.com/4Dv15/4D/15.4/SET-DATABASE-PARAMETER.301-3274410.ja.html)の``Debug log recording (34)``で出力したログファイルを解析するためのツール

## Info Report

**環境情報**や**キャッシュメモリ**の状態を記録して解析するためのツール

最新版は[ここ](https://taow.4d.com/Tool-4D-Info-Report/PS.1938271.en.html)から入手することができます。

[インストール方法](https://github.com/4D-JP/4d-developer-tools/blob/master/4D_Info_Report.pdf)

[説明書（英文）](https://github.com/4D-JP/4d-developer-tools/blob/master/4D_Info_Report_v4_9_Ref_v23.pdf)

[v14ダウンロード](https://github.com/4D-JP/4d-developer-tools/blob/master/4D_Info_Report_v4_9rZ_v14.zip)

[v15ダウンロード](https://github.com/4D-JP/4d-developer-tools/blob/master/4D_Info_Report_v4_9rZ_v15.zip)

[v16ダウンロード](https://github.com/4D-JP/4d-developer-tools/blob/master/4D_Info_Report_v4_9rZ_v16.zip)

* On Server Startupメソッドに記述

```
ARRAY TEXT($at_Components;0)
 COMPONENT LIST($at_Components)
 If(Find in array($at_Components;"4D_Info_Report@")>0)
  //5分毎にレポートを作成するストアドプロシージャを開始する
    EXECUTE METHOD("aa4D_NP_Schedule_Reports_Server";*;5;0)
 End if
 ```
