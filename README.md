# Server Monitoring Environment

[Grafana](https://grafana.com/ja/)による可視化 & [Prometheus](https://prometheus.io/)によるデータ収集でお家のラズパイサーバーを監視しよう～のリポジトリ

## Setup

`custom.ini.example`から`custom.ini`を作って値を入れてください(これがGrafanaログイン時のUser & Passwordになります。)

### 監視システム側

```
$ docker compose --profile admin up -d
```

### 監視対象ノード側

```
$ docker compose --profile exporter up -d
```

### prometheus.yml

https://itpfdoc.hitachi.co.jp/manuals/3021/30213L0600/IMRB0228.HTM

ローカルIPはハードコードしてます。監視対象が増えたら追加するスタイルで
