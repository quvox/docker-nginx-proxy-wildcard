Let's Encryptのワイルドカード証明書簡単取得ツール
=====

dockerを動かすだけで、ワイルドカード証明書を取得できる。取得した証明書は、cert/の下に格納される

### 前提
* ConoHa VPSを利用することを前提にしている（他にも対応しているらしいが）
* ConoHa DNSで対象ドメインのゾーンを管理するのでConoHa DNSにドメインを追加し、独自ドメインのサブドメインへのNSレコードをConoHa DNSに向けるように設定しておくこと。
* ConoHa APIでDNSレコードを操作するので、APIユーザを作成しておく。


## 初回取得
1. env.sampleを.envにコピーして中身を編集する
2. docker-compose -f newcert.yml up


## 更新
1. .envおよびcerts/は、元のものと同じにしておく
2. docker-compose -f renew.yml up

