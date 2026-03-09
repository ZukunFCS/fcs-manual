## Window

ウィンドウを表示するメニューです。ここでは各ウィンドウの説明を行います。

<details>
<summary><strong style="font-size: 1.5em;">Videos</strong></summary>
Videosウィンドウが開きます。

Videosウィンドウでは読み込んだHMC動画を一覧で表示します。読み込んだ動画に対しての処理も右クリックから可能です。
  
```{figure} /images/06_glossary_Menu_window_videos_window.jpg
:width: 80%
:align: center
```

①　Filter入力欄 \
動画名を文字列でフィルターします。

②　Importボタン \
ダイアログを開いて新しい動画をインポートします。シフトキーで複数選択が可能です。

③　Video表見出し \
右クリックメニューから表示する内容を変更することができます。

④　選択ON/OFF \
バッチ処理の対象にするかどうか切り替えます。

⑤　動画名 \
動画名を右クリックでメニューが表示されます。 \
メニューから単体のアニメーション出力などを行うことができます。

⑥　選択ON/OFF(全) \
Videosウィンドウのすべての動画に対して選択のON/OFFを切り替えます。

⑦　Removeボタン \
Remove Videos and Sequencesウィンドウを表示します。

<strong>Videos 右クリックメニュー</strong>

```{figure} /images/06_glossary_Menu_window_right_click.png
:width: 80%
:align: center
```

- 動画名
- Open \
動画を開く（PlayerとTimelineに表示されます）
- Remove \
Remove Videos and Sequencesウィンドウを表示します。

<strong>Remove Videos and Sequencesウィンドウ</strong>

```{figure} /images/06_glossary_Menu_window_remove_videos.png
:width: 80%
:align: center
```

オプションを指定して動画をFCSから削除します。

- Video \
動画名
- Delete caches option \
キャッシュデータについて
- ☑ SetData \
セットデータ内のファイル（音声・静止画連番）も削除するかどうか
- ☑ Tracking Sequence \
動画のトラッキングデータも削除するかどうか
- Profiles \
削除対象の動画から追加したプロファイルについて
   - プルダウンメニュー
   - Keep \
プロファイルはそのまま維持します
   - Keep but unlink \
プロファイルは維持しますが、動画との関連付けは削除します \
（プロファイルの動画名がUnkownになります） 
   - Delete \
  すべて削除します
- Execute \
実行
- Cancel \
キャンセル

```{note}
動画の尺変更などが原因で同じ名前の違う内容の動画を読み込みたいとき、
Keep＞再読み込みとするとピックアップしたフレーム位置にずれが発生し想定していないアニメーション結果になる場合があります。
適宜DeleteやKeep but unlinkで以前の動画との連携を解除してください。
```

</details>

- Processor
- Controllers
- Profiles \
Gallery \
Editor
- Solver 
- Log






