# Pre-rendering
あらかじめHTMLを作っておくこと。プリレンダリングにはSSGとSSRの二種類がある

# SSG(Static Site Generation)
HTMLがビルド時に生成され、各リクエストに再利用される。ビルド時にデータを読み込む必要がある場合は、getStaticProps関数と、getStaticPaths関数を使用する。

## 使用場面
ビルド時に一度だけフェッチし、ビルド後にデータを変更することができないため、ビルド後にデータの変更が必要ないページで使用される。  
※ 「ユーザのリクエストより先にこのページを Pre-rendering することができますか？」の質問に YES の時 SSG を使う

# SSR(Server Side Rendering)
HTMLがリクエストの度に生成される。リクエストが発生する度にHTMLを生成するため、SSGに比べて処理速度は遅くなるが、リクエストごとに最新の情報を入手できる。getServerSideProps関数を使ってフェッチする。

## 使用場面
ユーザーのリクエストなしでは Pre-rendering できないページ、最新情報を取得したい時に使用される。

参考動画  
[初めてのNext.js入門！簡単なアプリ実装でNext.jsを基礎から学んでみよう](https://www.youtube.com/watch?v=eEP7CLqnRr0&t=1202s)  
参考資料  
[SSG と SSR で理解する Next.js のページレンダリング](https://zenn.dev/luvmini511/articles/1523113e0dec58)
