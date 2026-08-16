# DFR0548-pwm1526

DFRobot micro:Driver(DFR0548)用の MakeCode スケッチ雛形。
[marugotoassist/pxt-motor](https://github.com/marugotoassist/pxt-motor)(DFRobot/pxt-motor のフォーク、日本語ブロック付き)を
拡張機能として導入済み。

**PWM 周波数を micro:Driver(PCA9685)の上限 1526Hz に設定済み**。
「最初だけ」ブロック内で `PWM周波数を設定 1526 Hz` を呼んでいる。
既定の 50Hz 版は [DFR0548-pwm50](https://github.com/marugotoassist/DFR0548-pwm50)、
1526Hz+起動ブースト+最低速度補正版は [DFR0548-pwm1526-kick](https://github.com/marugotoassist/DFR0548-pwm1526-kick) を参照。

> このページを開く [https://marugotoassist.github.io/DFR0548-pwm1526/](https://marugotoassist.github.io/DFR0548-pwm1526/)

## このプロジェクトを編集します

MakeCode でこのリポジトリを編集します。

* [https://makecode.microbit.org/](https://makecode.microbit.org/) を開く
* **読み込む** をクリックし、 **URLから読み込む...** をクリックしてください
* **https://github.com/marugotoassist/DFR0548-pwm1526** を貼り付けてインポートをクリックしてください

## 注意

* 1526Hz は PCA9685 のハードウェア上限(プリスケーラ最小値 3、内蔵 25MHz 発振)。
  これより高い値を指定しても 1526Hz に丸められる。
* 同じ PCA9685 をサーボと共用しているため、**この設定では RC サーボは正常動作しない**(サーボは 50Hz 前提)。
* 別の周波数を試すときは「最初だけ」内の数値を書き換えるだけでよい(24〜1526Hz)。

## 拡張機能について

`pxt.json` の `motor` 依存は marugotoassist/pxt-motor の特定コミットに固定してある。
フォーク側を更新したら、ハッシュを新しいコミットに差し替えること。

## 関連

* 実験計画: robotcar リポジトリ `2026/pxt-motor-pwmfreq/README.md`
* 参考にした雛形: [scramble-robot/DFR0548-Japanese](https://github.com/scramble-robot/DFR0548-Japanese)
