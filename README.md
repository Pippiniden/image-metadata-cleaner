# Image Metadata Cleaner

ブラウザ内で画像メタデータを削除する静的Webツールです。ビルド工程や外部ライブラリは不要です。

## GitHub Pagesで公開

1. GitHubで新しいリポジトリを作成します。
2. このフォルダ内の `index.html`、`.nojekyll`、`README.md` をリポジトリのルートにアップロードします。
3. **Settings → Pages** を開きます。
4. **Deploy from a branch** を選択します。
5. Branchを `main`、フォルダを `/(root)` にして **Save** を押します。
6. Pages画面に表示されるURLで利用できます。

## 対応形式

- JPEG / JPG
- PNG
- WebP

複数画像を処理すると、成功した画像を `cleaned_images.zip` にまとめてダウンロードします。

## プライバシーと処理

画像処理は利用者のブラウザ内で実行します。画像ファイルをサイトのサーバーへアップロードしません。

- JPEG: EXIF、XMP、Photoshop/IPTC系APP領域、コメント領域を除去
- PNG: テキスト系チャンク、EXIF、日時チャンクを除去
- WebP: EXIF、XMPチャンクを除去
- 画像データは再圧縮せず、ICC色プロファイルなどは保持する設計です

## 注意

すべての独自形式・未知のメタデータを完全に検出できるとは限りません。元画像を保管し、処理後の画像も確認してください。
