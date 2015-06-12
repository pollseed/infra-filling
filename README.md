infra code
---
インフラコードを詰め込ム

### セットアップ＆挙動確認

#### 未開の地

```.sh
vagrant init --minimal ubuntu/trusty64
vagrant up # 初回は1時間位かかる想定(OSインストールしてるからね)
vagrant box update # updateがあった場合は、最新にする(developerのOSは全部揃える)→1時間ぐらいかかったりする
vagrant ssh
```

#### このレポジトリを使う

```.sh
vagrant up
vagrant ssh
```
