# CTFにおけるpwnの攻略方法のメモ

## 1. 必要な知識

　バイナリの解析技術。

## 2. 必要なツール

　gdb、IDA、等

## 3. 攻略方法

　まずは、バイナリがどのような実行形式なのか `checksec -f` で、確認する。

  CanaryとNXが無効な場合は、スタックオーバーフローが可能。
  No RELRO/Partial RELROの場合は、GOT Overwriteが可能。