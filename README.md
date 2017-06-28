# 4d-developer-tools
開発者向けのツール


* On Server Startupメソッドに記述

```
ARRAY TEXT($at_Components;0)
 COMPONENT LIST($at_Components)
 If(Find in array($at_Components;"4D_Info_Report@")>0)
  //5分毎にレポートを作成するストラドプロシージャを開始する
    EXECUTE METHOD("aa4D_NP_Schedule_Reports_Server";*;5;0)
 End if
 ```
