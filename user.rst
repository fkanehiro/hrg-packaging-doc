=====================================
 HRG packagingの利用方法(ユーザ向け)
=====================================

はじめに
========

HRG packagingはlaunchpadのPPAサービスを使って、hrpsys-base, choreonoid, OpenHRPなどのロボット関連ソフトウェアの最新版を容易にインストールできるようにしたパッケージです。

初期設定
========

launchpadのPPAサービスを利用するにはadd-apt-repositoryコマンドが必要です。

ubuntu 12.04や12.10では以下のコマンドでインストールします::

  $ sudo apt-get install python-software-properties

ubuntu 14.04以降では以下のコマンドでインストールします::

  $ sudo apt-get install software-properties-common

add-apt-repositoryコマンドがインストールできたら、以下のコマンドでPPAを登録してください::

  $ sudo add-apt-repository ppa:hrg/daily

ppa:hrg/dailyには最新(daily build版)のパッケージが登録されています。より更新頻度の低い安定版のパッケージをインストールするには、以下のコマンドでstable版のPPAを登録してください::

  $ sudo add-apt-repository ppa:hrg/stable

パッケージのインストール
========================

パッケージをインストールするにはapt-getコマンドを使います。

例えば以下のコマンドを入力するとhrpsys-baseとその依存パッケージをインストールできます::

  $ sudo apt-get update
  $ sudo apt-get install hrpsys-base

OpenHRPをインストールしたい場合は::

  $ sudo apt-get install openhrp

choreonoidをインストールしたい場合は::

  $ sudo apt-get install choreonoid

とパッケージ名の部分を読み替えてください。


パッケージのアップデート
========================

パッケージをアップデートするにはapt-getコマンドを使います。

例えば以下のコマンドを入力するとhrpsys-baseをアップデートできます::

  $ sudo apt-get update
  $ sudo apt-get install hrpsys-base

また、以下のコマンドを入力することですべてのパッケージをアップデートできます::

  $ sudo apt-get update
  $ sudo apt-get upgrade


パッケージのアンインストール
============================

パッケージをアップデートするにはdpkgコマンドを使います。

例えば以下のコマンドを入力するとhrpsys-baseをアンインストールできます::

  $ sudo dpkg -r hrpsys-base
