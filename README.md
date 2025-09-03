# 音声入力テスト用ページ (GitHub Pages 向け)

- 全画面テキストエリア + 「クリップボードへコピー」ボタンのシンプルなページです。
- あなたの Chrome 拡張（音声入力）をこのページ上で動作確認できます。

## 使い方

1. この `index.html` を GitHub Pages で公開してください（`main` ブランチの `docs/` に置くか、`gh-pages` ブランチを使うなど）。
2. 公開 URL を Windows 常駐アプリ側の「設定 → サイトURL」に貼り付けて保存してください。
3. ページ下部の「クリップボードへコピー」を押すと、テキストエリアの内容がクリップボードへ入ります。
4. ネイティブアプリ側で <kbd>Ctrl</kbd>+<kbd>V</kbd> などでペーストしてください。

### クリップボード API の要件

- `navigator.clipboard.writeText()` は **HTTPS**（GitHub Pages等）または **localhost** で、かつ **ユーザー操作（クリック）** が必要です。
- 非対応環境では互換用に `document.execCommand('copy')` を試みますが、ブラウザにより動作しない場合があります。
