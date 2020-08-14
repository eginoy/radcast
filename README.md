# radcast

radikoを録音し、podcast配信する

radicastを少し、自分好みに改造しました
* <s>無劣化録音</s> → MP3コンバート復活
* 05時開始番組が録音できないときがある
* チャンネルのアイコン設定
* 番組のアイコン取得
* 他

ORIGINAL By https://github.com/soh335/radicast


## 必要パッケージ

* rtmpdump
* swftools
* ffmpeg or avconv

## インストール

```
$ go get github.com/omiso46/radcast
```

## 使い方

### 設定ファイル

```
$ radcast --setup > config.json
$ vim config.json
$ cat config.json

{
  "FMT": [
    "0 0 17 * * *"
  ]
}
```

cron specification is [here](https://godoc.org/github.com/robfig/cron#hdr-CRON_Expression_Format)

### 設定ファイルのリロード

```
$ kill -HUP nnn
```

## LICENSE

* MIT
