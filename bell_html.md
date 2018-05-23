# 発車メロディスイッチ再現

## 駅(JR)で使用されている発車メロディのスイッチをHTML上で再現してみたものです。

<div style="text-align: left">スイッチのイメージ↓</div>
<img src="https://lh4.googleusercontent.com/2gykHa90LLMMS1d3rRmvcWmajSbHtf1q3xtpaaFP8M7noH133Ju9inwqQMIGoa1AGR4f-KxZZzBwe74w1Jxg1h7aOUBp07-G8ytws8CHTosvi9B1JSK0rj12ZIS-hqqsq_Se83-1" title="発車ベルスイッチ" width="30%" heigh="30%">


[発車メロディサイト"github.io"使用](https://youk720.github.io/melo_work/melo.html)

<div style="text-align: right;"> ↑が実際に製作したものです </div>

<img src="/image/スクリーンショット 2017-12-20 16.47.35.png" width="30%" height="30%">

<div style="text-align:left;">スクショ画像</div>

- 基本的には”ON”を押すことによってメロディが再生され、OFFが押されるまではメロディはループを続けます。
- OFFボタンの下の”通常””立川式””ノン被り式”については以下記載
    - 通常選択時(デフォルト設定)はその時点でメロディを停止し戸閉放送が再生されます。
    - 立川式選択時はループを止めてかつ、その時点で戸閉放送を流しますが、メロディ終了まではメロディは流れ続けます。
    - ノン被り式選択時はループを止めて、メロディが終了してから戸閉放送を流します

- ”普通””戸閉放送ストップ”スイッチについて
  - 通常選択時(デフォルト設定)はOFFを押して戸閉放送が流れている時にONを押した場合メロディと被ります
  - 戸閉放送ストップ選択時はOFFを押して戸閉放送が流れている時にONを押した場合は、戸閉放送を止めてメロディが優先して流れます。
- ”メロディ選択”にてメロディの音源を選択し
- ”戸閉放送”にてOFFを押してからの放送音源を選択できます



## 使用機材
- Mac Book

## 使用ソフト
- Atom

## 製作期間
- 2017年10月頃から12月初旬

## コメント
- JavaScriptは大抵Googleで検索してそれを参考にしていたのですが、それをjQueryに対応させるように仕様を変更する時にエラーを出してたのですが、うまく行った時の達成感はすごかったです。

## 参考文献
https://qiita.com/kazu56/items/36b025dac5802b76715c

https://mae.chab.in/archives/2307

http://cly7796.net/wp/javascript/examined-the-jquery-of-key-events/
