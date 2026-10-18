# Yutori Matsugami — Web Card

GitHub Pages向けの、英語メイン・日本語補助のWeb名刺です。ページ本体は **index.html単体** で動作し、CSS・JavaScript・QR生成コード・フォントを内包しています。ビルド・npm・フォントの外部読み込み・CDNは不要です。

## ファイル

- index.html：ページ本体。ダークモード、スマホ表示、メール・URLコピー、共有用QR、対応端末でのOS共有。
- ogp.png：SNSのリンクプレビュー用画像（1200 × 630）。ページ本体の表示には不要ですが、画像付きの共有に使います。
- ogp.svg：OGP画像の編集用原稿。
- DESIGN.md：参考サイトとデザイン方針。
- .nojekyll：GitHub Pagesで静的ファイルをそのまま配信するための設定。
- tools/embed-fonts.py：本文を編集したときに、埋め込みフォントを更新するための任意ツール。通常の公開・閲覧には使いません。

index.htmlはダブルクリックで確認できます。ファイル直開きやlocalhostでは、公開URLへのQRとURL共有を表示しません。公開したページでは、そのページ自身のURLからQRを生成します。閲覧者のURLを外部QRサービスへ送信しません。

## GitHub Pages公開手順

### 1. 公開先

この版は、次のユーザーサイトで公開する設定にしています。リポジトリ名は **yutorimatsugami.github.io** です。

    https://yutorimatsugami.github.io/

リポジトリが既にある場合は、既存の内容や公開設定を確認してから追加してください。

### 2. SEO・OGP用のURLを確認する

canonical・og:url・JSON-LDのURLは **https://yutorimatsugami.github.io/**、og:image・twitter:imageは **https://yutorimatsugami.github.io/ogp.png** に設定済みです。別の公開先へ移す場合は、これらの値も更新します。

共有用QRとコピーするURLは公開ページのURLから生成されます。

メタ情報はJavaScriptによる後付けではなく、元のHTMLに記述しています。

### 3. ファイルをアップロードする

GitHubで公開先リポジトリを用意し、ルートに少なくとも次を置きます。

    index.html
    ogp.png
    README.md
    .nojekyll

ogp.svgとDESIGN.mdも、原稿として一緒に置けます。.previewフォルダーは確認用なので公開用ファイルには含めません。

GitHubの **Add file → Upload files** からアップロードし、mainブランチへ保存できます。

### 4. Pagesを設定する

1. リポジトリの **Settings → Pages** を開きます。
2. **Build and deployment → Source** を **Deploy from a branch** にします。
3. ブランチを **main**、フォルダーを **/ (root)** にして **Save** します。
4. デプロイ完了後、Pages設定に表示される公開URLを開きます。
5. **Enforce HTTPS** が利用可能なら有効にします。

リポジトリの可視性・利用プランによってPagesの利用条件が変わる場合があります。画面の表示を優先してください。

公式手順：
- [GitHub Pagesサイトを作成する](https://docs.github.com/ja/pages/getting-started-with-github-pages/creating-a-github-pages-site)
- [GitHub Pagesサイトの公開元を設定する](https://docs.github.com/ja/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

### 5. 公開後に確認する

- スマホで横スクロールせず読めること。
- GitHub・X・Hugging Face・ORCID・Emailの各リンク。
- Shareを開き、別のスマホでQRを読み取れること。
- QRのURLにlocalhost、REPOSITORY_NAMEなどが入っていないこと。
- 「公開URL + ogp.png」が表示できること。
- SNSへURLを貼ったときのタイトル・説明・画像。SNS側のキャッシュで更新に時間がかかることがあります。

## 掲載情報と更新箇所

公開メールは、ご本人指定の **ok230200@oks.iput.ac.jp** です。メールを変更する際は本文のリンク・コピー用のJS変数・JSON-LDをまとめて変更してください。

2026年度4年生・2023年4月開始という整理に基づき、ページでは「2023–present」とコース名で表記しています。所属・在籍状況に変化があれば更新してください。

Hondaの記載は **Job offer / 技術職 内定** です。在職や入社済みという表記ではありません。入社後のメールアドレスは未設定です。

研究の英語見出し「VLM-based affordance representation」は、このページ用の要約です。正式な日本語題名も併記し、リンクの名称は論文本体ではなく **Conference program** としています。

大会の順位はチーム実績です。2025年の本人参加はご本人からの申告、順位は大会公式結果・大学公式記事に基づいています。中高生時代の大会名・出場年・個人賞は追加していません。

### 出典

確認日：2026-10-18

- [ORCID公開記録](https://orcid.org/0009-0009-7290-9276)
- [RSJ2026公式プログラム、31ページ・3L1-03](https://ac.rsj-web.org/2026/wp-content/uploads/2026/08/RSJ2026_pg_0827_detail.pdf#page=31)
- [SAM3 Learningless AI Vision](https://github.com/yutorimatsugami/sam3-learningless-ai-vision)
- [実習先の開発記事](https://3up-tec.jp/challenge/sam3-learningless-ai-vision/)
- [RoboCup JapanOpen 2026 @Home公式結果](https://sites.google.com/site/robocuphomejapan/japanopen2026/results)
- [RoboCup JapanOpen 2025 @Home公式結果](https://sites.google.com/site/robocuphomejapan/japanopen2025/results)
- [2025年大会の大学公式記事](https://www.iput.ac.jp/eyes/10674/)
- [ワオラボ神戸三宮教室・メンター紹介](https://www.waolab.jp/sannomiya/)
- [西澤育英基金・第4期奨学生の掲載](https://www.nishizawa-sf.org/introduction/)
- [大学公式の内定者インタビュー](https://www.iput.ac.jp/eyes/12211/)

## QRコード生成コード

index.htmlに [QRCode.js](https://github.com/davidshimjs/qrcodejs) を内包しています。MITライセンス。著作権表示と許諾条件はHTMLのスクリプト内に保持しています。実行時の外部依存はありません。

## フォントとOGPの編集

英字は [Inter](https://rsms.me/inter/)、日本語は [Noto Sans JP](https://fonts.google.com/noto/specimen/Noto+Sans+JP) です。年や小さなラベルには端末標準の等幅フォントを使っています。InterとNoto Sans JPのWOFF2データをHTMLに埋め込んでいるため、オフラインでも指定した書体で表示できます。著作権表示とSIL Open Font License 1.1の全文をHTMLとSVG内に保持しています。

容量を抑えるため、フォントは使用する文字・ウェイト400〜500に絞っています。新しい漢字などを追加すると、その文字は端末のフォントで補われる場合があります。編集後に以下を実行すると、本文とOGPに必要な文字を含め直せます。これは編集者向けの処理で、公開時のビルドは不要です。

```sh
python3 -m pip install 'fonttools[woff]'
python3 tools/embed-fonts.py
```

ツールはバージョンを固定したGoogle Fonts公式リポジトリのフォントを取得し、チェックサムを確認します。取得データは公開対象外の.preview/font-cacheに保存します。

OGPは変更できます。ogp.svgの文字・色・図形を編集し、1200 × 630のPNGとして書き出してogp.pngを差し替えます。原稿にもフォントを埋め込んでいます。英字はInter、日本語はNoto Sans JPです。Chromeでの表示を確認しています。編集ソフトによっては埋め込みフォントを使えない場合があるので、書き出し後の画像を確認してください。文字を変更したときは、PNGの書き出し前に上記のツールを実行します。

公開後の差し替えはSNS側のキャッシュによって反映が遅れることがあります。
