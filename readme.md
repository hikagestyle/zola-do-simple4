# まえがき

Zola（静的サイトジェネレーター）のテーマ。

個人的なファイル一式。

修正や加工ほか、ご利用は自己責任で。


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


## 基本的なコマンド
- ローカルチェック
	- zola serve
	- zola serve --drafts
	- zola --help
	- zola --version

- ビルド
	- zola build
	- zola build --drafts


## 完成イメージ

デモサイト: https://zola-do-simple4.netlify.app/


## 公式サイト

- [Zola](https://www.getzola.org/)
- [Pure](https://purecss.io/)

