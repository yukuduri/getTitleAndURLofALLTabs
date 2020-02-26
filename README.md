# getTitleAndURLofALLTabs
 開いているウインドウ内のすべてのタブのタイトルとURLを取得するGoogleChrome拡張機能です。
 
 # 機能紹介
 現時点ではまだ設定を変える機能は未実装なので直接`JavaScript`のコードを弄ることになりますが、今後、設定を変えられるようにする予定です。
 
 ## テンプレート機能
`getTitleAndURL.js`15行目の変数を書き換えることで、コピーしたいタイトル、URLの形式（コロン区切りやMarkDown形式など）に変えることができます。

%%title%%：ページのタイトルに置換されます。  
%%URL%%：ページのURLに置換されます。  
仕様上、「'」「"」「\」を含めるには、エスケープシーケンス「\'」「\"」「\\」を用いる必要があります。

例えば、MarkDown形式に対応させる（そのまま貼り付けて使えるようにする）には、`[%%title%%](%%URL%%)`のようにします。デフォルトでは、`[%%title%%](%%URL%% \"%%title%%\")`となっており、`a`タグの`title`属性を付与させています。

## 区切り文字編集機能
`getTitleAndURL.js`15行目の変数を書き換えることで、一つ一つのページのタイトル&URL間の区切りを指定できます。これにより、コンマ区切りなどにもできます。デフォルトでは改行となっています。

## メイン機能：開いている全てのタブのページ情報のクリップボードへのコピー
getTitleAndURLofALLTabsを動かしたウィンドウ内の全てのページのタイトルとURL（テンプレートと区切り文字に基づく）を表示し、「copy」ボタンのクリックでクリップボードにコピーすることができます。


# 参考文献
今回、拡張機能を作成するにあたって参考にさせていただいたページを、以下に貼り付けさせていただきます。
多くの記事を参考にさせていただきました。ありがとうございます。

[ページのタイトルとURLを取得するChrome拡張を作った。 - Qiita](https://qiita.com/a01sa01to/items/bd7b18b4ec3dc6c46b32 "ページのタイトルとURLを取得するChrome拡張を作った。 - Qiita")  
[Chrome 拡張機能のマニフェストファイルの書き方 - Qiita](https://qiita.com/mdstoy/items/9866544e37987337dc79#options_page "Chrome 拡張機能のマニフェストファイルの書き方 - Qiita")  
[Chromeブラウザの拡張機能を作ってみたい初心者向けに開発方法を紹介！【サンプルあり】 - Qiita](https://qiita.com/guru_taka/items/37a90766f4f845e963e5 "Chromeブラウザの拡張機能を作ってみたい初心者向けに開発方法を紹介！【サンプルあり】 - Qiita")  
[Chrome拡張機能作成〜超基礎編〜 - Qiita](https://qiita.com/Ryo_Suzuki/items/d247008888ef67bdeda8 "Chrome拡張機能作成〜超基礎編〜 - Qiita")  
[特定の文字列を全て置換する[Javascript] - Qiita](https://qiita.com/DecoratedKnight/items/103ab57431b6c448e535 "特定の文字列を全て置換する[Javascript] - Qiita")  
[Chromeアドオン開発のチュートリアル：　ページの背景色を変えるアドオン（Getting Started Tutorial） - 主に言語とシステム開発に関して](https://language-and-engineering.hatenablog.jp/entry/2018/10/22/Chrome%E3%82%A2%E3%83%89%E3%82%AA%E3%83%B3%E9%96%8B%E7%99%BA%E3%81%AE%E3%83%81%E3%83%A5%E3%83%BC%E3%83%88%E3%83%AA%E3%82%A2%E3%83%AB%EF%BC%9A_%E3%83%9A%E3%83%BC%E3%82%B8%E3%81%AE "Chromeアドオン開発のチュートリアル：　ページの背景色を変えるアドオン（Getting Started Tutorial） - 主に言語とシステム開発に関して")  
[クリップボードとのやりとり - Mozilla | MDN](https://developer.mozilla.org/ja/docs/Mozilla/Add-ons/WebExtensions/Interact_with_the_clipboard "クリップボードとのやりとり - Mozilla | MDN")  
[EventTarget.addEventListener() - Web API | MDN](https://developer.mozilla.org/ja/docs/Web/API/EventTarget/addEventListener "EventTarget.addEventListener() - Web API | MDN")  
[chrome.windows - Google Chrome](https://developer.chrome.com/extensions/windows#current-window "chrome.windows - Google Chrome")  
[Declare Permissions - Google Chrome](https://developer.chrome.com/extensions/declare_permissions "Declare Permissions - Google Chrome")  
[The activeTab permission - Google Chrome](https://developer.chrome.com/extensions/activeTab#what-activeTab-allows "The activeTab permission - Google Chrome")  
[chrome.windows-Google Chrome](https://developer.chrome.com/extensions/windows#property-WINDOW_ID_CURRENT "chrome.windows-Google Chrome")  
  

あ、これは以前私が書いた記事ですが、一通りまとまっているので自分でも重宝しています。  
[JavaScript基礎文法 - Qiita](https://qiita.com/yukuduri/items/cff4a1f9c85114600425 "JavaScript基礎文法 - Qiita")  