# myled
ロボットシステム学　課題1

2021年度ロボットシステム学で作成したデバイスドライバを改良した物です。

# 動作環境
･Raspberry Pi3 ModelB+

･Ubuntu 20.04 

# 使用品
･Raspberry Pi3 ModelB+

･LED ×2

･ブレッドボード

･ジャンパー線（オス-メス）×4

# pin情報
LED1(黄):22 (動画右側)

LED2(黄):24 (動画左側)

# インストール
以下のコマンドを実行

$ git clone git@github.com:hoteiy/myled1.git

$ cd myled1

$ make

$ sudo insmod myled.ko

$ sudo chmod 666 /dev/myled0

# アンインストール
以下のコマンドを実行

$ sudo rmmod myled

# 実行方法
$ echo 0 > /dev/myled0　LED1、LED2消灯

$ echo 1 > /dev/myled0　LED2点灯

$ echo 2 > /dev/myled0　LED1点灯

$ echo 3 > /dev/myled0　LED1、LED2点灯

$ echo 4 > /dev/myled0　LED1、LED2が交互に点灯、消灯を20回繰り返す

# 実行動画
https://youtu.be/fieD3l6RQQI

# ライセンス
GNU General Public License v3.0
