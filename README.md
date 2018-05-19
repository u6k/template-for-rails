# Template for Rails _(template-for-rails)_

[![standard-readme compliant](https://img.shields.io/badge/readme%20style-standard-brightgreen.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)

> 自分流のRuby on Railsプロジェクトを開始する手順

__Table of Contents__

<!-- TOC depthFrom:2 -->

- [Background](#background)
- [Requirement](#requirement)
- [Steps](#steps)
  - [やりたいことをREADMEに書く](#やりたいことをreadmeに書く)
  - [RedmineとGitHubにプロジェクトを作成する](#redmineとgithubにプロジェクトを作成する)
    - [プロジェクトの命名](#プロジェクトの命名)

<!-- /TOC -->

## Background

Railsプロジェクトを「いつもの構成で」「素早く」開始するために、このテンプレートがあります。このテンプレートの手順を実行すると、次の要件のRailsプロジェクトを開始します。

- 開発環境、本番環境
  - Docker
    - ホスト環境を言語処理系で汚さないため、Dockerコンテナで作業します
    - ホスト環境にはDockerとエディターがあれば良いです
- 言語処理系、フレームワーク、RDBMS
  - Ruby v2.5
  - Ruby on Rails v5.2
  - PostgreSQL v10
    - MySQLでも良いです
    - 開発時から本番環境と同じRDBMSを使用します
- ログ出力
  - ログレベル
    - development, test
      - DEBUGレベル
    - production
      - INFOレベル
  - 出力先
    - STDOUT
- ドキュメント
  - README
    - standard-readme
    - Readme Driven Development
  - CHANGELOG
    - Keep a Changelog

次の要件は必須ではありません。必要に応じて適用してください。

- ビルド環境
  - TravisCI
- プロジェクト管理
  - u6k.Redmine
    - GitHubで管理するとは限らないため
- ソースコード管理
  - GitHub
  - BitBucket
  - GitLab
    - 基本的にはGitHubで管理します
- Dockerイメージ管理
  - Docker Hub

## Requirement

- Docker
  - 筆者のOS環境はWindowsですが、他OSでも問題ありません。

```
$ docker version
Client:
 Version:      18.03.1-ce
 API version:  1.37
 Go version:   go1.9.5
 Git commit:   9ee9f40
 Built:        Thu Apr 26 07:12:48 2018
 OS/Arch:      windows/amd64
 Experimental: false
 Orchestrator: swarm

Server:
 Engine:
  Version:      18.03.1-ce
  API version:  1.37 (minimum version 1.12)
  Go version:   go1.9.5
  Git commit:   9ee9f40
  Built:        Thu Apr 26 07:22:38 2018
  OS/Arch:      linux/amd64
  Experimental: false
```

## Steps

Railsプロジェクトを開始する手順を説明します。

### やりたいことをREADMEに書く

まず、困っていること、やりたいこと、最初に欲しい最小限の機能をREADMEに書きます。ここで多く書きすぎた場合は、別プロジェクトに切り出せば良いだけなので、頭の中を空っぽにする勢いで書き出します。次の記事を参考にすると良いです。

- [Readme Driven Development](http://tom.preston-werner.com/2010/08/23/readme-driven-development.html)
- [Readme駆動開発を和訳してみた - Qiita](https://qiita.com/syossan27/items/38e2f4b7f0dc74207dc9)

READMEテンプレートは、[RichardLitt/standard-readme: Standard Readme Style](https://github.com/RichardLitt/standard-readme)を使用します。

やりたいことを整理するために、企画チケットを作成して構想を練っても良いです。

### RedmineとGitHubにプロジェクトを作成する

やりたいことを整理したら、GitHubにリポジトリを作成します。速度が大事なWebの世界では、さっさとオープンにすることが大事。また、同様のプロジェクトが既に存在しても、それが十分に知名度を持っていない限り、あまり気にしなくても良いです。

次の設定でGitHubリポジトリを作成します。

- Repository Name
  - 命名には十分に注意します(後述)
- Description
  - 当プロジェクトを1文で表現します
- Initialize this repository with a README: チェック
- Add .gitignore: None
- Add a license: MIT License
- Website
  - 次に作成するRedmineプロジェクトの概要ページのURLを設定します

次に、Redmineにもプロジェクトを作成します。

- 名称: GitHubリポジトリのRepository Nameと同じ
- 説明: GitHubリポジトリのDescriptionと同じ
- 識別子: 名称と同じ
- ホームページ: GitHubリポジトリのURL
- 公開: チェック
- モジュール
  - チケットトラッキング
  - ニュース
  - Wiki
  - Knowledgebase
- トラッカー
  - 機能
  - サポート
  - バグ
- メンバー
  - 自分を「管理者」「開発者」「報告者」として追加

#### プロジェクトの命名

プロジェクトの命名には十分に注意します。公開してドメイン名も取得してしばらくしてから名称でもめると、非常に面倒なことになります。ただ、しばらくは知名度が低いはずなので、まずはランダム・ネーム・ジェネレーターで命名してしまい、v1.0リリースの時にリネームしても良いかもしれません。

- [Random Word Generator - Word+](http://watchout4snakes.com/wo4snakes/Random/RandomWordPlus)
- [WORDOID - Creative Name Generator - Domain names, company names, product names](http://wordoid.com/)

命名の方法論は、多くの素晴らしい記事があるので(つまり、それだけ多くの人が命名で悩んでいます)、それらを参考にしても良いです。

- [The essential guide to choosing good project names](https://www.articulatemarketing.com/blog/project-names)
- [Igor Naming Guide Naming Companies](https://www.igorinternational.com/process/naming-guide-product-company-names.php)
- [Naming Your Software Project in 5 Minutes or Less | Slaptijack](https://slaptijack.com/programming/naming-your-software-project-in-5-minutes-or-less/)

