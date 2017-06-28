# 4d-developer-tools
開発者向けのツール

### Info Report

最新版は[ここ](https://taow.4d.com/Tool-4D-Info-Report/PS.1938271.en.html)から入手することができます。

* On Server Startupメソッドに記述

```
ARRAY TEXT($at_Components;0)
 COMPONENT LIST($at_Components)
 If(Find in array($at_Components;"4D_Info_Report@")>0)
  //5分毎にレポートを作成するストアドプロシージャを開始する
    EXECUTE METHOD("aa4D_NP_Schedule_Reports_Server";*;5;0)
 End if
 ```
