TechTrain環境
===================================

## 環境構成
### Provision 
Puppet
## Set Up 
### git clone
```
$ git clone git@github.com:hironomiu/VagrantTechTrain.git
or
$ git clone https://github.com/hironomiu/VagrantTechTrain.git 
```
### 起動

- 起動

```
$ cd VagrantTechTrain  
$ vagrant up  
```

## Login
### techtrain
```
$ ssh techtrain@192.168.56.120
```
### vagrant
```
$ vagrant ssh
```
## users

| OS user | pass | 接続DB | 接続Port |  DB user |  DB pass | 用途 |
|:-----------:|:------------:|:------------:|:------------:|:------------:|:------------:|:------------:|
| root | - | - | 3306 |  root | vagrant | root vagrantユーザより sudo su -にて遷移|
| vagrant | - | - | - | - | - | vagrant用ユーザ vagrant sshにてログイン|
| techtrain | techtrain | techtrain | 3306 | techtrain | techtrain | 開発ユーザ |

## Packages   
### MySQL
- 5.6
- 自動起動
```
/etc/my.cnf
```
 
### iptables
- 自動起動
- port22,80 allow

### httpd
- 自動起動
- DocumentRootは適時設定すること

### PHP
- 5.4
