
## vagrant-global-status
ホスト端末内の仮想端末の情報をまとめて一覧表示。

## 操作
$ vagrant global-status --all

## sahara
サンドボックスというスナップショットをとっておき、好きな時にそこまでロールバックできる。というもの

### sandboxモード開始（時間がかかるからVagrantを停止してから行ったほうが良い）
$ vagrant sandbox on

### 変更を決定する（時間がかかるからVagrantを停止してから行ったほうが良い）
$ vagrant sandbox commit

### 変更を破棄し、ロールバックする
$ vagrant sandbox rollback

### sandboxモード終了（commitしていないものは破棄される）
$ vagrant sandbox off

### 現在sandboxモードかどうかの確認
$ vagrant sandbox status
