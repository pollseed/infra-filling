infra code
---
インフラコードを詰め込ム

### 事前準備
バージョンに関してはなるべく合わせる  
古いバージョンのせいでエラーになることが多々ある

#### 対象環境

* MacOS == 10.10.3
* Homebrew == 0.9.5
* Python >= 2.7
* Ruby >= 2.2

#### インストール

* vagrant == 1.7.2
* virtualbox == 4.3.28
* ansible >= 1.9.1

```.sh
# install
brew cask install vagrant
brew cask install virtualbox
brew install ansible

# version
vagrant -v
ansible --version
```

### セットアップ＆挙動確認

#### 未開の地

重いなら、OSのイメージ使ってKURE

```.sh
vagrant init --minimal ubuntu/trusty64
vagrant up # 初回は1時間位かかる想定(OSインストールしてるからね)
vagrant box update # updateがあった場合は、最新にする(developerのOSは全部揃える)→1時間ぐらいかかったりする
vagrant ssh
```

#### このレポジトリを使う

```.sh
cd vagrant/
vagrant up
vagrant box list
vagrant ssh-config --host harmox > ~/.ssh/config
vagrant ssh
```
#### frequency cmd

| cmd | detail |
|:--:|:--:|
|`vagrant halt`|停止|
|`vagrant reload`|再起動|
|`vagrant status`|状態|

### 作ったあとに適応したい時

```.sh
vagrant provision
```
