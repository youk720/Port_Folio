#Tone()を使ってシンセ作ってみる

## 製作期間
  - 2018年5月10日〜

## きっかけ
  - 上のメロディのものを作ってて、スイッチで選曲を変えるものを作ろうとしていたら,TAより「これでシンセ作ってみたらいいんじゃない？」ということで作ってみようと思ったから

##　実験
  - まず、13個ものスイッチを扱うため、分圧回路でピン数を節約するため、実験してみた
    - <img src="/image/IMG_4826.JPG" width="30%" height="30%">
    - ↑ブレッドボード組み立て風景
    - <img src="/image/IMG_4832.JPG" width="30%" height="30%">
    - ↑回路図
    - 成功
  - 次に、実際つけるボタンを配置確認
    - <img src="/image/IMG_4822.JPG" width="30%" height="30%">
    - ピアノ風に配置
  - コードはこんな感じ
    - <img src="/image/スクリーンショット 2018-05-10 14.45.05.png" width="20%" height="20%">
    - [コード]((https://github.com/youk720/arduino_led/blob/master/melody/sw/sw.ino)
  - 動作確認後,ユニバーサル基板にて半田付け
    - <img src="/image/IMGP0112.JPG" width="40%" height="40%">

## 感想
  - 一本の入力ピンで13ものスイッチを作動させるのは思った以上に簡単だったが、コンソール向けのコードを描くのに苦労したが、そのコードが思った以上に単純すぎて興味深かった？

## 参考文献
  -  https://synapse.kyoto/tips/ResDiv/page001.html
  -  http://www.mech.keio.ac.jp/ja/souzou/proceedings2014/pdf/4-10.pdf
  -  http://myy.github.io/blog/2013/09/27/make-instrument-with-tact-switch/
