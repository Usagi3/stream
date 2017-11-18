# Stream

ローカル環境限定でWebRTCでLIVE配信できます。
npm install を使うのでnpmが動作する環境を整えてください

## 内容物

```
.
├── README.md        // 本ファイル
├── bin              // 実行ファイル 
├── broadcaster.html // 配信者側html
├── index.html       // 視聴者側html
├── node_modules     // node_modules
└── signaling.js     // シグナルサーバ
```

## インストール

1. 本プログラムをhttp://~でアクセスできるところに設置する

2. npm install
```
./bin/install.sh
```

3. 動作環境に合わせてIPを変更する

変更するファイル

* broadcaster.html
* index.html

"192.168.10.103"の部分を自分の環境にあわせて変更する

## 動作方法

1. コンソールからシグナルサーバを起動

```
node signaling.js
```

2. 配信者側

Firefoxから以下のURLにアクセス
http://192.168.10.103/stream/broadcaster.html

"192.168.10.103"は動作環境に合わせる

「Start Video」をクリックして配信を開始

3. 視聴者側

Firefoxから以下のURLにアクセス
http://192.168.10.103/stream/

"192.168.10.103"は動作環境に合わせる

「Request」をクリックして視聴を開始