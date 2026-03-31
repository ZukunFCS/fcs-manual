## Window

FCSを構成する各機能ウィンドウの役割と、それぞれの表示制御や操作方法について説明します。  

```````{tab-set}

``````{tab-item} Window

`````{grid} 1 1 2 2 
:gutter: 3
:items-align: top

````{grid-item}
:child-align: top

```{image} /images/06_glossary_Menu_Window.jpg
:width: 100%
```

````

````{grid-item}
① Videos：  
動画の読み込みや処理に関するウィンドウ  

② Processor：  
動画の複数処理に関する設定を行うウィンドウ  

③ Controllers：  
controller登録に関するウィンドウ  

④ Profiles/Gallery：  
登録済みのProfileに関するウィンドウ  

⑤ Editor：Profile登録に関するウィンドウ  

⑥ Solver：  
出力の詳細設定に関するウィンドウ  

⑦ Log：FCSのログを表示するウィンドウ  
````


`````



````{list-table}
:widths: 50 50
:header-rows: 0

* - ```{figure} /images/06_glossary_Menu_Window.jpg
     :width: 100%
     :align: center
    ```
  - ① Videos：HMC動画など動画の読み込みや処理に関するウィンドウ
    
    <br>

    ② Processor：動画の複数処理に関する設定を行うウィンドウ
    
    <br>

    ③ Controllers：controller登録に関するウィンドウ

    <br>

    ④ Profiles/Gallery：登録済みのProfileに関するウィンドウ

    <br>

    ⑤ Editor：Profile登録に関するウィンドウ

    <br>

    ⑥ Solver：出力の詳細設定に関するウィンドウ

    <br>

    ⑦ Log：FCSのログを表示するウィンドウ

````

<br>

``````


``````{tab-item} Videos

Videosウィンドウが開きます。  

Videosウィンドウでは読み込んだHMC動画を一覧で表示します。  
読み込んだ動画に対して、右クリックで開くメニューで個別の設定・処理が可能です。  

```{figure} /images/06_glossary_Menu_window_videos.jpg
:width: 100%
:align: center
```

<br>

① Filter入力欄：動画名で絞り込み  

② 【Import】：新しい動画のインポート  
　押すとダイアログが開き、動画を選択できます。
　シフトキーで複数選択が可能です。  

③　Video表見出し
　右クリックメニューから表示する内容を変更可能です。    

④　選択ON/OFF：バッチ処理対象の切り替え  

⑤　動画名  
　右クリックでメニューが表示し、単体のアニメーション出力などを行うことができます。  
　※詳細は『videos/右クリックメニュー』をご確認ください。  

⑥　選択ON/OFF(全)：すべての動画に対して選択のON/OFFの切り替え  

⑦　Removeボタン：「Remove Videos and Sequences」ウィンドウを表示  

<br>

```{rubric} **Videos 右クリックメニュー**
```



```{list-table}
:widths: 40 60
:header-rows: 0

* - ![](/images/06_glossary_Menu_window_right_click.jpg)
  - 1. **動画名**
    2. **Open**
       動画を開く（PlayerとTimelineに表示されます）
    3. **Remove**
       「Remove Videos and Sequence」ウィンドウを表示します。
```


Remove Videos and Sequencesウィンドウ

```{figure} /images/06_glossary_Menu_window_remove_videos.jpg
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
動画の尺変更などが原因で、同じ名前・違う内容の動画を読み込みたいとき、ProfilesをKeepにして該当の動画を削除＞動画を再読み込みすると、ピックアップしたフレーム位置にずれが発生し、想定していないアニメーション結果になる場合があります。
適宜DeleteやKeep but unlinkで以前の動画との連携を解除してください。
```

Process

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

**出力画面説明**

```{figure} /images/03_workflow_export_animation_process_list.jpg
:width: 80%
:align: center
```

▼Process

☑ Reprocess：作成したProfile情報を読み取る

```{note}
基本的に ☑ を付けることをオススメします。
```

Upload Options
-  ☑ Animation：アニメーションデータを生成、Mayaに反映
-  ☑ Audio：解析する動画の音声データをMayaに反映
-  ☑ Frames：解析する動画の連番画像を生成、Mayaのイメージプレーン上に反映
-  ☑ Landmark Frames：顔の動きをオートトラッキングする連番画像を生成、Mayaのイメージプレーン上に反映

Export Options
-  ☑ Playblast：出力されたアニメーションをmov形式の動画で出力、保存する
-  ☑ Scene：出力されたMayaシーンを自動で保存する

Start process：アニメーションの出力を開始する


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





``````



`````{tab-item} Processor

<br>

Processerウィンドウが開きます。  

Processerウィンドウでは複数の動画を一括で処理するバッチ機能が使用できます。  
VideosウィンドウでチェックボックスがONになっている動画が処理の対象になります。  
  
```{figure} /images/06_glossary_Menu_window_processor.jpg
:width: 100%
:align: center
```

<br>

①　**Output Folder**：出力先を指定  

②　**Output Targets**：出力する内容を指定  
　・☑ Animation：アニメーションデータを出力  
　・☑ Audio：音声データをMayaに読み込む  
　・☑ Frames：動画の連番画像を出力し、Mayaのイメージプレーンに読み込む  
　・☑ LM Frame：ランドマーク付の連番画像を生成し、Mayaのイメージプレーンに読み込む  
 　※ "++パイプライン"では使用不可  
　・☑ Playblast：プレイブラストをmov形式の動画で出力し、保存  
　・☑ Scene：Mayaシーンを保存  
　・Format：出力するMayaの保存形式を指定(.mb / .ma)  

③　**Advanced**：出力処理の詳細設定  
　・☑ Reprocess：キャッシュが既に存在する場合も一から解析する  
　・Output Filename：出力されるデータ名を指定  

<br>

```{rubric} **フォルダ名・動画名を指定するパラメータ**
```

<br>

<!--start_here_Processor_01-->

```{note} 
Output Filenameを変更することで出力ファイル名に任意の名前を設定できます。  

- {solver} ： solverの名前
- {video} ： ビデオのファイル名
- {user} ： windows ユーザ名
- {project} ： 案件フォルダ名
- {chara} ： キャラクター名
- {actor} ： 役者名
- {%Y%m%d}, {%H%M%S} ： 年月日、時間分秒  

{video}のみにするとimportした動画名で出力されます。
```

<!--end_here_Processor_01-->

<br>

④　**【Start】**：アニメーションの出力を開始  

⑤　**プログレスバー**：処理状況の表示  

⑥　**Log**：処理状況のログを表示


<br>


`````



`````{tab-item} Controllers

コントローラーの登録に関するウィンドウです。

```{figure} /images/06_glossary_Menu_window_controller.jpg
:width: 80%
:align: center
```


① Filter：入力したコントローラー名で絞り込み  
② 【all▼】：コントローラーの絞り込み  
　all / null / upper / lower / gaze / eyelid  指定した項目を絞り込んで表示します。  

```{note}
- Region名（upper / lower / gaze / eyelid）：  
現在登録しているRegionのコントローラーが表示されます。  
プルダウンがRegionの状態でAdd Selectedを押すと、  
コントローラーをそのRegionに設定された状態で読み込むことができます。  

- all：すべてのRegionのコントローラーが表示されます。  
allの状態でコントローラーを読み込むとRegionにはnull(リージョン未設定)が設定されます。  

- null：リージョンが設定されていないコントローラーが表示されます。  
コントローラー表に一つでもnullがあると登録したコントローラーを保存できないため、  
Save前にリージョンがnullになっているコントローラーがないか確認してください。　　

```
<br>

③ Maya/Add selected：Maya上で選択したコントローラーを登録  
④ ☑ Sync：数値操作をMayaと連動させる  
　例：⑧min/max、⑨default などの数値操作  

⑤ ☑ ：選択  
⑥ コントローラー名：登録したコントローラー名一覧  
　右クリックで個別のメニューを表示します、詳細は下記「**コントローラー名→右クリック**」をご確認ください。  

⑦ Region：各コントローラーの設定したRegionの表示や調整
　【Region(画像ではupper) ▼】で個別にRegionを変更できます。  

⑧ min/max：コントローラーの最小値・最大値の表示や調整
```{note}
最大値最小値は自動で入力されますが、値があまりにも大きすぎる場合は調整を行って下さい。
```

⑨ default：コントローラーのデフォルト値の表示や調整

⑩ 【▼Value】：☑ を入れたコントローラーの値を調整  
　・ ▼Min / Max / Default：どの数値を調整するか  
　・ 0.000：入力する数値  
　・ Apply：入力した数値をコントローラーに反映  

⑪ 【▼Region】：☑ を入れたコントローラーにRegionを設定  
　upper / lower / gaze / eyelid  
　→ 押下したRegionに設定します。  

⑫ Remove：☑ を入れたコントローラーを表から削除  

⑬ 【Select All】：表示されているコントローラーすべてに ☑ を入れる
⑭ 【Unselect All】：表示されているコントローラーすべてからチェック □ を外す  

⑮ 【▼Advanced】
　・【Remove empty】：Regionが登録されていないコントローラー(null)を表から削除  
　・【Delete all】：登録したコントローラー情報をすべて削除  
　・【Reset】：直前に【Save】した状態に戻す  
　・【Rename】：「Replace controllers」ウィンドウを開く  
　　※詳細については下記「**複数コントローラーの一括リネーム**」を参照ください。  
　・ ☑ Rearrange：コントローラー表の順番をドラッグ＆ドロップで変更できるようにする  

⑯ 【save】：controllersの変更を保存しcontroller Infoに登録  

<br>

```{rubric} **コントローラー名→右クリック**
```
一覧からコントローラー名を右クリックすることで、メニューが表示されます。  


```{figure} /images/06_glossary_Menu_window_controller_click.jpg
:width: 80%
:align: center
```

<br>

① 【▼Copy&Paste】  
　・【Copy Name】：コントローラー名をコピー  
　・【Copy Values】：数値操作をコピー  
　・【Copy Blendshapes】：ブレンドシェイプをコピー  
　・【Paste Values】：数値操作貼り付け  
　・【Paste Blendshapes】：ブレンドシェイプを貼り付け  

<br>

② 【▼Reset】  
　・【To Save】：名前・数値などを【Save】時点に戻す  
　・【To Maya】：名前・数値などをMayaの設定に戻す  

<br>

③ 【Rename】：コントローラー名の変更  
 「Rename controller」ウィンドウが開くので、「New Name」に変更したい名前を入れ、  
 【Rename】を押します。  
    
```

<br><br>


```{rubric} **複数コントローラーの一括リネーム**
```

リネームしたいコントローラーに ☑ をいれ、【▼Advanced】→【Rename】を押します。  
すると「Replace controllers」ウィンドウが開きます。  

```{figure} /images/06_glossary_Menu_window_controller_Rename.jpg
:width: 80%
:align: center
```

<br>

① 【Add】：コントローラー名に文字列を追加    
　【front ▼】（front/back）：コントローラー名の前後どちらに追加するかを指定します。  

② 【Replace】：コントローラー名の指定の文字列を置き換え    
　→『**変換前の文字列**』with『**変換後の文字列**』　をそれぞれ入力します。  

③ Preview：コントローラー名の変換前後のプレビュー    
　①・②それぞれ【Add】【Replace】を押すと、プレビューが表示されます。  

④【Save】：リネームを反映  
　③のPreviewを確認し、問題なければ【Save】を押し反映させます。  

<br>

`````


`````{tab-item} Profiles/Gallery

**Galleryの画面説明**

```{figure} /images/03_workflow_create_profile_gallery_explanation.jpg
:width: 80%
:align: center
```
作成したProfileが表示されるウィンドウ

&larr;&rarr;：1列に表示するprofileの数を変更する。◀を押すと少なく、&rarr;を押すと多くなる。最小3、最大10。
Count:○○：登録しているprofileの総数

All&darr;：該当する項目を絞り込む
- All：すべてのprofileを表示する
- Enabled：解析に使用するprofileを表示する。Enabledに ☑ を入れて登録したprofileが対象となる。
- Disabled：解析に使用しないprofileを表示する。Enabledに ☑ を入れずに登録したprofileが対象となる。
- Default：数値がdefaultのprofileを表示する。
- Not Default：数値がdefaultではないprofileを表示する。
- Neutral：Neutralにチェックを入れて登録したprofileを表示する。
- （Region）Enabled：該当する（Region）に ☑ を入れて登録したprofileを表示する。
- （Region）Disabled：該当する（Region）に ☑ を入れず登録したprofileを表示する。

Sync timeline ☑ ：登録したprofileと同じ動画を開いた状態でprofileを選択すると、該当するフレームにジャンプする。

&uarr;&darr;：ソートの昇順 降順を変更する

Video▼：ソート機能
- Video：profileのName順にソート
- Created At：profileを作成した日時で順にソート
- Saved At：saveした日時で順にソート
- （controller名）：該当する（controller）に登録した数値でソート
  
ピックアップした画像
- 緑：「Neutral」に ☑ を入れて登録したProfile  
- 赤：数値がデフォルト状態/未編集のProfile  
- 青：選択中（編集中）のprofile  
- 黒：「Enabled」の ☑ を外し、「Disabled」で登録したprofile  
- 白：リターゲット後、登録したprofile 


```{figure} /images/06_glossary_Menu_window_gallery.jpg
:width: 80%
:align: center
```

<strong>Gallery</strong>

- Count \
現在表示されているプロファイル数を表示します。
- [ 　 ]▼
   - Enabled \
Enabled状態のプロファイルを表示します。
   - Disabled \
Disabled状態のプロファイルを表示します。
   - Default \
数値未設定含む、すべてのRegionがデフォルトの値のプロファイルを表示します。
   - Not Default \
デフォルトの値ではないプロファイルを表示します。
   - Neutral \
ニュートラルのプロファイルを表示します。
   - No Tags \
タグのついていないプロファイルを表示します。
   - [Region名] Enabled \
そのRegionに値が登録されているプロファイルを表示します。
- Sync timeline \
選択したプロファイルが含まれる動画を開いている場合、そのプロファイルのフレームに移動します。
- Adbanced \
詳細機能を表示します。

<strong>Misc</strong>

- Hide Tooltip
   - □ \
登録されているRegionの図の表示 / 非表示を切り替えます。
- Display Mode
   - Image \
プロファイルをアクターの写真で表示します。
   - Render \
プロファイルをキャラクターモデルのスクリーンショットで表示します。
- Refresh Renders \
Display Mode＞Render表示用にスクリーンショットを現在のMayaの設定で再出力します。


`````



`````{tab-item} Profiles/Editor


*Editorの画面説明**

```{figure} /images/03_workflow_create_profile_editor_explanation.jpg
:width: 80%
:align: center
```
Sync:
- To Maya：登録されているprofile情報をMayaに転送する
- From Maya at save：saveする際にMaya上での調整データを取得しFCSに反映する
- Both：FCSとMayaを双方向で連動させる
- No Sync：FCSとMayaを連動させない


- Neutral：デフォルトの表情として必ず1つ登録する
- Enabled：解析する素材として使用する

Controller▼
- Controller：コントローラー表示が名前になる
- Value：コントローラー表示が数字になる 

▼Region
- Upper/Eyelid/Gaze/Lower：調整した情報を登録する  

▼Utils
- To Maya：FCS上で操作した値をMayaへ送る
- From Maya：Mayaで操作した値をFCSへ送る
- Predict：画像から表情を解析し、Mayaの3Dモデルに反映する機能

LM：LandMarkを表示する  

▼Filter
- ▼all/Upper/Eyelid/Gaze/Lower：選択した項目でコントローラーを絞り込む
- [ ]：入力した文字でコントローラーを絞り込む  

▼Reset：入力した情報を削除する
- Name：Profileとして登録する名前
- Save：変更した情報を保存する
- 画像部分：Timelineから+で追加した画像が表示される
- コントローラー：Controller Infoで登録したコントローラーが表示される

Editor

プロファイルを登録するウィンドウです。 \
画像に対応する表情をMayaで作成し、FCSに読み込みます。

```{figure} /images/06_glossary_Menu_window_editor.jpg
:width: 80%
:align: center
```


- No Sync▼ \
数値の操作をMayaと同期させるかどうかの設定です。
   - To Maya \
FCSのスライダー上でのプロファイルの数値変更をMayaに転送します。
   - From Maya \
saveボタンを押す際にMaya上での表情データを取得しFCSに反映させてから登録します。
   - Both \
「To Maya」と「From Maya」をどちらも行い、FCSとMayaを双方向で同期させます。
   - No Sync \
FCSとMayaを同期させません。
- Neutral \
Neutral表情かどうかを設定します。
- Enabled \
このプロファイルを表情推定の計算に含めるかどうか設定します。
- Controller▼ \
プロファイル画像右のスライダー表記を切り替えます。
   - controller \
スライダーにコントローラー名を表示します。
   - Value \
スライダーに値を表示します。
- Name \
プロファイル名を表示します。任意の名前に変更することも可能です。
- save \
現在の設定でプロファイルを登録・保存します。

```{note}
コントローラーウィンドウ右部のスライダーはCtrl＋クリックで直接数値を入力することが可能です。
```

`````



`````{tab-item} TimeLine
**Timelineの画面説明**

```{figure} /images/03_workflow_create_profile_timeline.png
:width: 80%
:align: center
```
- Timeline：バーを左右に動かし、ビデオを手動で再生させる
- [0][20130]：ビデオの縮尺を変更できる。
- [7967]：現在のフレーム数
- |< >|：1フレーム前/後に移動する
- << >>：登録したprofileにジャンプする
- ＞ ||：動画の再生 - 停止（再生すると一時停止ボタンが表示される）
- Video：Video playerに表示されている動画名

`````


`````{tab-item} Solver


`````




`````{tab-item} Log

FCS上で表示されたログを確認できます。  

```{figure} /images/06_glossary_Menu_window_Log.jpg
:width: 80%
:align: center
```
<br>

① 【WARNING ▼】：表示するログの種類を選択
　・INFO：インフォメーションログを表示  
　・WARNING：警告ログを表示  
　・ERROR：エラーログを表示  

② Time：発生時刻  

③ Logeer

④ Level：ログの種類　※①を参照ください。  

⑤ Message：ログの詳細・メッセージ内容  



**最新のログについては常にFCS下部に表示されます。**  

```{figure} /images/06_glossary_Menu_window_Log02.jpg
:width: 80%
:align: center
```

<br>


`````

`````{tab-item} Player
`````


`````{tab-item}　Timeline
`````



```````

<br>

```{rubric} **Menu説明 目次**  
```

```{include} index.md
    :start-after: <!--start_here-->
    :end-before: <!--end_here-->
```






