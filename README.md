# ansible-bigip
ansibleでBIG-IPを操作するModuleを使ったPlabookサンプル。

# 注意事項
趣味で作成したので動作の保証はしない。各モジュールのドキュメントのサンプルを確認して検証環境で試験をしてほしい。

# 想定構成
2台でHA構成となっているBIG-IP VEで2台のWebサーバをバランシングする構成を想定
## BIG-IP VE
Version : 13.x
## Ansible
Version : 2.9.x

# サンプル
## bigip-facts.yml
2台のBIG-IPから構成情報を収集する。`gather_subnet:`で収集する情報を指定可能

## disable_pool_member.yml
特定のPoolからメンバーを1台disableにし、冗長構成のBIG-IPに対して自身のコンフィグを配布し同期する

## enable_pool_member.yml
`disable_pool_member`のenable版

