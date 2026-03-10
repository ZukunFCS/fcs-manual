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
:width: 40%
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

<strong>Process</strong>

```{figure} /images/06_glossary_Menu_window_process.jpg
:width: 80%
:align: center
```

- ☑ Reprocess \
キャッシュが既に存在する場合も一から解析します
- Sequence Options \
Sequence Name \
シーケンスの名前を設定します
- Upload Options
   - ☑ Animation \
アニメーションデータを出力します
   - ☑ Audio \
音声データをMayaに読み込みます
   - ☑ Frames \
動画の連番画像を出力、Mayaのイメージプレーンに読み込みます
   - ☑ LM Frames \
ランドマーク付の連番画像を生成、Mayaのイメージプレーンに読み込みます \
（+パイプラインでは使用不可）
- Export Options
   - ☑ Playblast \
プレイブラストをmov形式の動画で出力、保存します
   - ☑ Scene \
Mayaシーンを出力、保存します
   - Start processing \
上記の設定で処理を実行します

<strong>Copy</strong>

```{figure} /images/06_glossary_Menu_window_copy.png
:width: 40%
:align: center
```

- Filename \
動画のファイル名をクリップボードにコピーします
- Full path \
動画のフルパスをクリップボードにコピーします
- Parent \
動画の親ディレクトリのパスをクリップボードにコピーします

</details>

<details>
<summary><strong style="font-size: 1.5em;">Processor</strong></summary>
Processerウィンドウが開きます。

Processerウィンドウでは複数の動画を一括で処理するバッチ機能が使用できます。
VideosウィンドウでチェックボックスがONになっている動画が処理の対象になります。
  
```{figure} /images/06_glossary_Menu_window_processor.jpg
:width: 80%
:align: center
```

①　Output Folder \
出力先を指定します

②　Output Targets \
出力する内容を指定します
   - ☑ Animation \
アニメーションデータを出力する
   - ☑ Audio \
音声データをMayaに読み込む
   - ☑ Frames \
動画の連番画像を出力、Mayaのイメージプレーンに読み込む
   - ☑ Landmark Frames \
ランドマーク付の連番画像を生成、Mayaのイメージプレーンに読み込む \
（+パイプラインでは使用不可）
   - ☑ Playblast \
プレイブラストをmov形式の動画で出力、保存する
   - ☑ Scene \
Mayaシーンを保存する
   - Format \
出力するMayaの保存形式(.mb / .ma)
   - ☑ Distribute

③　Advanced
   - ☑ Reprocess \
キャッシュが既に存在する場合も一から解析する
   - Output Filename \
出力されるデータ名

④　Start \
アニメーションの出力を開始する

⑤　プログレスバー \
処理状況の表示をします

⑥　Log \
処理状況のログが表示されます

<strong>フォルダ名・動画名を指定するパラメータについて</strong>

- {solver} \
solverの名前
- {video} \
ビデオのファイル名
- {user} \
windowsユーザ名
- {project} \
案件フォルダ名
- {chara} \
キャラクター名
- {actor} \
役者名
- {%Y%m%d} \
年 月 日
- {%H%M%S} \
時間 分 秒

</details>

- Controllers
- Profiles \
Gallery \
Editor
- Solver 
- Log








