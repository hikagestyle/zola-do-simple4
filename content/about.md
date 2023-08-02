+++
title = "あばうと"
date = 2022-01-01T00:00:00+09:00
template = "static.html"
+++

あばうとのページ。

<img src="../images/1920x1080.jpg" alt="サンプル画像" width="50%">

これは<span style="color: red; ">赤文字</span>です。


![サンプル画像](../images/1920x1080.jpg)

画像は「static/images」へ入れて管理していく方針。

固定ページと記事投稿は、相対リンクの階層が異なるので、記述に注意する。

記事投稿
- ../../images/xxx.jpg
- `![テキスト](../../images/xxx.jpg)`

固定ページ
- ../images/xxx.jpg
- `![テキスト](../images/xxx.jpg)`


## 環境

- パソコン: X230（Lenovo ThinkPad）
- OS: Linux Mint 20.3（Xfce）
- Zola v0.17.2


## 補足

サクッと使う個人的な用途で小規模を想定。

blogフォルダへ投稿を詰め込んで、タグで仕分けるイメージ。

Zolaで個人的に使うシンプルなテーマ。

短時間で作ったので、大雑把にやっつけです。

zola-do-simple3 を Zola v0.17.2 に対応させた自作テーマ。


## 基本的な仕様

ドメイン直下、サブディレクトリでも、とりあえず使えるはず。（config.tomlのbase_urlによる）

- pure.css
- config.toml
	- base_url（最後のスラッシュ無し）
- カテゴリー無し
- タグ（taxonomies）有効
	- 日本語のタグ付けは、zolaの仕様で自動的に英数字へ変換される
- ページ送り:デフォルトで10件ごと
	- content/blog
- タグのページ送り:デフォルトで5件ごと
	- config.tomlから変更可
	- テンプレートの場所:templates/tags/single.html
- 投稿のURL=ファイル名（.mdファイル）
- 固定ページのテンプレート（デフォルト:日付表示なし）
	- 日付表示はコメントアウト
	- templates/static.html
- メニューページ（固定ページ）


## GitHub

基本的なファイル一式はGitHubに置いておきます。

規模や好みでチョイス。


- このサイトと同じテーマ
	- <a href="https://github.com/hikagestyle/zola-do-simple4" target="_blank" rel="nofollow noopener noreferrer">zola-do-simple4</a>
- zola-do-simple3(Zola v0.15.2)
	- <a href="https://github.com/hikagestyle/zola-do-simple3" target="_blank" rel="nofollow noopener noreferrer">zola-do-simple3</a>
- タグのページ送り有り
	- <a href="https://github.com/hikagestyle/zola-do-simple2" target="_blank" rel="nofollow noopener noreferrer">zola-do-simple2</a>
- タグのページ送り無し
	- <a href="https://github.com/hikagestyle/zola-do-simple" target="_blank" rel="nofollow noopener noreferrer">zola-do-simple</a>


## このテーマの基本的な使い方

- config.tomlの編集
	- base_url（最後にスラッシュ無し）
	- title
	- description
- templatesを必要に応じて編集
	- _analytics.html
	- _sidebar.html
	- index.html
- 投稿をする（記事作成、ページ作成）
	- content/blog（記事作成、タグ付け可）
	- content（ページ作成、タグ付け不可）
- ローカルチェック
	- zola serve
	- zola serve --drafts
- ビルド
	- zola build
	- zola build --drafts
- publicフォルダが生成される


## ビルドまでの流れ

投稿のURL=ファイル名（.mdファイル）

シンプルに「content/blog」へ記事作成（.md）をしてビルド。（タグ付け可）

固定ページは「content」にページ作成（.md）をしてビルド。（タグ付け不可）

