# ansible-isucon/isucon4-qualifier

## Overview

Ansible playbook for [ISUCON4-qualifier](http://isucon.net/archives/41252218.html)

## Requirement

- CentOS 6.x

## Usage

Remote:
```
git clone https://github.com/matsuu/ansible-isucon.git
cd ansible-isucon/isucon4-qualifier
echo 192.0.2.1 > hosts
ansible-playbook -i hosts playbook.yml
```

Local:
```
yum install -y epel-release git
yum install -y ansible
git clone https://github.com/matsuu/ansible-isucon.git
cd ansible-isucon/isucon4-qualifier
ansible-playbook -i local playbook.yml
```

Vagrant:
```
$ vagrant up
```

## 本来の設定と異なるところ

- MySQLのバージョンを5.5.42からMySQL GA最新版(現在は5.6系)に変更しています
- nginxのバージョンを1.6.1からstable最新版に変更しています
- ログインユーザをec2-userからvagrantに変更しています
- ベンチマークプログラムのインスタンスチェックを削除しています
- Ruby 2.3.3 instead of 2.1.3 which finished its support. NOTE: I haven't checked apprecation behaviours with this change.
- Go1.1 instead of Go1.3.

## References

- [ISUCON4(2014) オンライン予選レギュレーション](http://isucon.net/archives/39979344.html)
- [ISUCON4 予選当日マニュアル](https://gist.github.com/mirakui/e394ed543415852d34a6)
- [isucon/isucon4](https://github.com/isucon/isucon4)
- [vagrant-isucon](https://github.com/matsuu/vagrant-isucon)
