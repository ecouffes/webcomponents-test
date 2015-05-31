# Web component test用リポジトリ

## Web Componentの構成要素
```bash
# Template
ブラウザネイティブのテンプレート
<template>要素内に、テンプレートとなるHTMLとCSSを記述。

# Cumtom Elements
ブラウザ解釈可能なカスタム要素
カスタム要素には、プロパティ・メソッド・イベントの定義が可
基本は、DOM APIのHTMLElementオブジェクトを拡張
（既存要素からも拡張可能）
カスタム要素名には「−」を含め、前方互換性（将来追加される可能性があり得る
　　　新要素とのバッティング防止）を確保。

# Shadow DOM
カプセル化された隠匿DOM
（スコープで守られたDOM）
カスタム要素内のCSSは、スコープ化されており、グローバルDOMに影響を与えない。

# HTML Imports
<link rel=“import” href=“components/hoge.html”>
とコンポネントコードを読み込みんで使用する。
※この機能を試すためには、要ローカルサーバ。

## ローカルサーバ＆起動方法(mac)
$ cd webComponent_test-master
$ python -m SimpleHTTPServer

## chrome、および、それ以外のモダンブラウザでの比較
http://localhost:8000/
http://localhost:8000/polyfill.html
http://localhost:8000/excss.html

