# Predict_calorie_from_photos
## 概要
予め設定したカロリーにはなるが、写真を選択すると、これに対応するカロリーが選択される機械学習アルゴリズムを作成する。カロリーの数値と、写真は自分で変更可能である。

## Flicker APIを使用する
### KeyとSecretを取得

1. https://www.flickr.com/services/api/

2. ログイン後画面上部にあるcreate an App

3. 右のRequest an API

4. 目的に応じた方を選択する

5. 適当に入力

6. KeyとSecretを入手

### Flickr APIのモジュールをインストール

1. pip3 install flickrapi

2. download.pyで[Key]と[Secret]を書いて実行

3. image/指定フォルダ下にそれぞれダウンロードしてきた写真が保存されているので、クリーニング作業を行う

4. read_image.pyを実行し、写真を全てnumpy形式にして./image/に保存

※ ここからはpythonファイルか.ipynbファイルで行う

### .pyファイルの場合
1. cnn2.pyでmodelを作成
2. my_photo.pyで写真からカロリー予測を行う
※cnn.pyはCNNを使用した精度の低い練習モデル

### .ipynbファイルの場合
1. npzが正しくnumpyファイル形式で保存されているか確認している
2. 精度の低いCNNモデルを作成している(このモデルは使用していない)
3. 水増しを行ったCNNモデルを作成している(このモデルを使用している)
4. 対象写真を予測する


myphoto.pyかphotos.ipynbの最後の方の LABELSとCALORIESを書き換えることで、予測するカロリーのジャンルを変えることができる。



