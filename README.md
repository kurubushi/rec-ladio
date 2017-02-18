# rec-ladio

[ねとらじ](http://ladio.net/)を録音する．

あらかじめ用意しておいたマウントのリストを元に，
それらマウントの放送状況を監視し，録音．


## usage

```bash
./rec-ladio mount_list
```

`mount_list`に書き連ねたマウントを監視，録音．
放送に関する詳細情報をjsonとして保存．
デフォルトの保存場所は，`$HOME/Music/ladio/マウント名`．
`mount_list`の書式については，`mount_list_sample`を参照．

また，録音の途中で強制終了させた場合，
各マウント名ディレクトリに`.lock`ファイルが残るので，削除すること．


## config

適宜`rec-ladio`の定数を書き換え．

* `LADIO_PATH`  
    デフォルトの保存先
* `SLEEP_TIME`  
    監視の間隔
* `WGET_OPTS`  
    wgetへ渡すオプション


## depens

wgetに依存しています．
ほか，次が必要かも．

```bash
gem install json
```
