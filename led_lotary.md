# 中学時代に作ったフルカラーLチカを復活させる

## 使用機材
- Mac Book
- Maruduino UNO R3

<![プリント基板_実際](/image/IMG_4806.JPG)
 前に作った部品付きプリント基板↑

## 使用ソフト
- Arduino IDE

## 制作期間
- 2018年4月20日〜

## やったこと
- フルカラーLEDを制御
  - [コード](https://github.com/youk720/arduino_led/blob/master/RGB_LED_change.ino)
- ロータリーエンコーダがなかったので可変抵抗で代用して入力をコンソールで確認
  - [コード](https://github.com/youk720/arduino_led/blob/master/analogin_test.ino)
- 以上からLEDを可変抵抗で制御(↓コード)
  - [コード](https://github.com/youk720/arduino_led/blob/master/analogLED_control.ino)
- 可変抵抗により点滅速度を変える機能をつける、かつ今までの機能を温存
  - [コード](https://github.com/youk720/arduino_led/blob/master/2type_mod.ino)
- ![ユニバ基盤](/image/IMG_4301.JPG)
  - ↑今までのものをユニバーサル基板でつけたもの
- 基盤のピン番号を確認
  - [コード](https://docs.google.com/spreadsheets/d/18CofA8giMLeH86uY-xxpBrVRsyEB2kDP5-jguv-FJ60/edit?usp=sharing)
- ピン番号を元に発光させてみる
  - [コード](https://github.com/youk720/arduino_led/blob/master/print_led_test)
- プリント基板にあったLEDの並列つなぎ(詳しい人によるとダイナミック点灯というらしい)やってみた
  - ![ブレッドボード組](/image/IMG_4304.JPG)
  - 部品 緑LED 1kΩ*2で(500Ω分並列) ブレッドボード Arduino(電源扱い)
  - attachInterruptを使用しようと思ったが、それだと2つ以上のロータリーエンコーダを制御は難しい
  - ただ、それに基づいて測ってみた
- さっきの制御は忘れて一旦、チャタリング全て無視して3つのローたりでLED制御
  - [コード](https://github.com/youk720/arduino_led/blob/master/rotary_3led_cont.ino)
  - しかし、ロータリーエンコーダのB相はそれぞれのピンで分かれているが,A相が謎の部品を経由し同一ピンに集まる理由が不明でありかつ,どうスケッチを書くのか未だに謎、

# 一向に不明なため、いつかわかる時まで無期限保留

## コメント・感想
 - ロータリーエンコーダの仕組みはだいたい理解できていたが、今回の基盤の構造が高度すぎた？のと忘れてしまったのがかなり、痛い点だったと思う。
 - 次何を作ろう・・・
<!--
その他,メモ
Vin = 電源

指数関数的にLED変えれば自然に見える(らしい)
http://bey.hatenablog.com/entry/2016/10/18/004136 -->


## 参考文献
 - https://jumbleat.com/2016/12/17/encoder_1/#i-3
 - attachInterrupt 解説↓
  -  http://www.musashinodenpa.com/arduino/ref/index.php?f=0&pos=3069
  -  http://easylabo.com/2015/04/arduino/8357/
