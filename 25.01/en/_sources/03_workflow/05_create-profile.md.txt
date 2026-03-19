## Profileの作成

Profileを作成する前にまず使用する動画をFCSに読み込みます。

```{rubric} **解析動画をimportする**
```

Window&rarr;VideosでVideosウィンドウが開きます。  
Videosウィンドウでは解析したい動画を開いたり、インポートすることができます。
```{figure} /images/03_workflow_create_profile_windows_videos.jpg
:width: 80%
:align: center

Windows&rarr;Videos
```

```{figure} /images/03_workflow_create_profile_videos_import.jpg
:width: 80%
:align: center

Import
```

Importを押すとウィンドウがポップアップされるので、解析したい動画をクリックし開きます。   
```{figure} /images/03_workflow_create_profile_videos_open.jpg
:width: 80%
:align: center
```

<br>

```{note}
Shift+クリックで複数同時にimportできます。
```

<br>

```{figure} /images/03_workflow_create_profile_videos_complete.jpg
:width: 80%
:align: center

Videosウィンドウにimportした動画が表示されます。
```

<br><br>

```{rubric} **Profile（プロファイル）について**
```

様々な表示のProfileを追加することで解析の精度が上がっていきます。  
単純に数が多ければ良いわけではなく、似た表情のProfileに対し、コントローラーの数字が違ってしまった場合、ノイズになってしまうため注意が必要です。  
また、解析する動画毎にProfileを1つ以上作成することを推奨しています。  

```{note}
ROM体操と呼ばれる約50個のProfileの作成をオススメしています。  
ROM体操の表情については、スターターキット同梱のPDFファイルをご参照ください
```

<br><br>


```{rubric} **読み込んだ動画をFCSで開く**
```

開きたい動画ファイル名の上で右クリック　→　【Open】  
VideoPlayer上に動画が表示されます。  

```{list-table}
:widths: 50 50
:header-rows: 0

* - ![](/images/03_workflow_create_profile_right_click_open.jpg)

    動画ファイル名の上で右クリック　→　【Open】  

  - ![](/images/03_workflow_create_profile_video_player.jpg)

```

<br>


```{rubric} **Profileの追加方法**
```

VideoTimelineウィンドウの  
 - スライダーを動かし表情の登録を行いたいフレームで止め、【+】を押す。  
   Galleryに指定したフレームの画像が追加されます。
```{figure} /images/03_workflow_create_profile_profile_addition.jpg
:width: 80%
:align: center
```

<br>

```{note} プロファイルを追加した際の枠について  
赤：数値がデフォルト状態/未編集のProfile  

緑：「Neutral」に ☑ を入れて登録したProfile  

青：選択中（編集中）のprofile  

黒：「Enabled」の ☑ を外し、「Disabled」で登録したprofile  

白：リターゲット後、登録したprofile  
```

<br>

```{rubric} **Neutralの表情の登録**
```

Neutral表情とは、アクターの表情筋に力が入っていないナチュラルな表情のことです。  
セッション内で必ず一つNeutral表情を設定してください。 

 - Neutralに ☑  
 - 任意の名前に変更  
 - Save


```{list-table}
:widths: 50 50
:header-rows: 0

* - ![](/images/03_workflow_create_profile_neutral_save.jpg)

    NeutralのProfileは登録が完了すると緑になります。    

  - ![](/images/03_workflow_create_profile_neutral_complete.jpg)

```

<br><br>

```{rubric} **Mayaで表情を調整する場合**
```

VideoTimelineウィンドウのスライダーを動かし表情の登録を行いたいフレームで止め+を押す  
Galleryに指定したフレームの画像が追加されます。  
```{figure} /images/03_workflow_create_profile_gallery_addition.jpg
:width: 80%
:align: center

値が0（未登録）のProfileは赤枠
```

<br>

追加した赤色の画像をクリックし、Editor画面に表示されている画像が同じであることを確認
```{figure} /images/03_workflow_create_profile_image_confirm.jpg
:width: 80%
:align: center
```

<br>

Mayaのコントローラーリグで、追加したアクターの表情と同じになるようにキャラクターの表情を調節
```{figure} /images/03_workflow_create_profile_maya_character_adjustment.jpg
:width: 80%
:align: center
```

<br>

【From Maya】をクリックすると、Mayaでの調整情報がFCSに反映されます。
```{figure} /images/03_workflow_create_profile_from_maya.jpg
:width: 80%
:align: center
```

```{note}
Syncのプルダウンで「From Maya at save」もしくは「Both」にしている場合は、調整した数値が自動で同期されます。
```

```{note}
コントローラーの登録忘れがあった場合は再度開いたときに作成した表情と異なる場合があります。  
その際は、再度登録し忘れたコントローラーを登録しプロファイルの再登録を行ってください。
```

<br>

 - Nameを任意の名前に変更
 - Save
```{figure} /images/03_workflow_create_profile_image_name.jpg
:width: 80%
:align: center
```

<br>

```{note}
名前は必ずしも変更する必要はありません。
```

<br>

**ーーーーーーーーーーーー　以下未確認！　ーーーーーーーーーーーー**

```{rubric} **FCS上で表情を調整する場合**
```

VideoTimelineウィンドウのスライダーを動かし表情の登録を行いたいフレームで止め+を押す  
Galleryに指定したフレームの画像が追加されます。  
```{figure} /images/03_workflow_create_profile_gallery_addition.jpg
:width: 80%
:align: center

値が0（未登録）のProfileは赤枠
```

<br>

追加した赤色の画像をクリックし、Editor画面に表示されている画像が同じであることを確認
```{figure} /images/03_workflow_create_profile_image_confirm.jpg
:width: 80%
:align: center
```
 
 <br>


**Syncが「No Sync」の場合はProfileの自動情報共有が行われないためMaya上は1つ前に登録した表情のままになっています。**  
```{figure} /images/03_workflow_create_profile_maya_sync.jpg
:width: 80%
:align: center
```

```{note}
Syncを「Both」にした状態で開きなおすと デフォルトの表情になります。  
既にしている場合はスキップ
```

<br>

【Editor】上の【controller】で、追加したアクターの表情が同じになるようにキャラクターの表情を調節
```{figure} /images/03_workflow_create_profile_controller_adjustment.jpg
:width: 80%
:align: center
```

<br>

````{note}

```{list-table}
:widths: 40 60
:header-rows: 0

* - ![](/images/03_workflow_create_profile_filter.jpg)

  - 絞り込みたい項目（文字含む）のみ表示されるようにするには…  
    ▼Filterから搾りたい項目をクリック  
```

````

<br>

【To Maya】をクリック
```{figure} /images/03_workflow_create_profile_to_maya.jpg
:width: 80%
:align: center
```

<br>

```{note}
Syncのプルダウンで「To Maya」もしくは「Both」にしている場合は、調整した数値が自動で同期されます。
```

<br>

FCSで調整した内容がMayaに反映されます。
```{figure} /images/03_workflow_create_profile_maya_reflection.jpg
:width: 80%
:align: center
```

<br><br>

```{rubric} **Predict機能について**
```

本ソフトでは、作成したProfileから自動でリターゲットをしてくれる**Predict機能**を搭載しています。  
ある程度の数のProfileを登録した後で、追加のProfileを登録する際にPredict機能を使えば、  
登録済のProfileを基に、ソフトが予想した表情を作成してくれます。

```{warning}
Predictで自動リターゲットする精度は、登録済のProfileの精度と連動します。    
また、動画全体を解析するわけではないので注意が必要です。
```

<br>

VideoTimelineウィンドウのスライダーを動かし表情の登録を行いたいフレームで止め+を押す  
Galleryに指定したフレームの画像が追加される  
追加した赤色の画像をクリックし、Editor画面に表示されている画像が同じであることを確認  
```{list-table}
:widths: 50 50
:header-rows: 0

* - ![](/images/03_workflow_create_profile_gallery_addition.jpg)  

    Galleryに追加される  

  - ![](/images/03_workflow_create_profile_image_confirm.jpg)  

    Editor画面に表示されている画像が同じか確認する

```

<br>

**Predictを実行**  
valueの数値が変動します。
```{figure} /images/03_workflow_create_profile_predict.jpg
:width: 80%
:align: center
```

<br>

MayaにPredict結果が出るので、  
調整が必要な場合は調整し、登録できる内容になったら
```{figure} /images/03_workflow_create_profile_predict_confirm.jpg
:width: 80%
:align: center
```

<br>

【Save】する
```{figure} /images/03_workflow_create_profile_image_save.jpg
:width: 80%
:align: center
```

<br><br>

```{rubric} **Profileを作成するときの注意点**
```

**ーーーーーーーーーーーー　以下編集中　ーーーーーーーーーーーー**


**目を閉じる/薄目の時のGaze登録について**
```{warning}
目を閉じる、薄目のプロファイルで黒目が見えないものは登録する際にGazeの ☑ を外してください  
解析結果の精度が低下してしまう可能性があります  
```

例：眉のぎゅっと絞る動きを作りたい時には
```{figure} /images/03_workflow_create_profile_close_eyes.jpg
:width: 80%
:align: center
```

 - 表情を調整した上で
```{figure} /images/03_workflow_create_profile_close_eyes_adjustment.jpg
:width: 80%
:align: center
```

 - Regionのgaze/lowerの ☑ を外す
```{figure} /images/03_workflow_create_profile_close_eyes_region.jpg
:width: 80%
:align: center
```

 - Save

**解析結果が好ましくない場合**
```{warning}
解析する動画は、必ず1動画1profile以上作成するようにしてください
Profileを作成していない場合、精度が十分ではない解析結果が出力される可能性があります 
```
Videosウィンドウの「Profiles」をご参照ください    
```{figure} /images/03_workflow_create_profile_videos_profiles.jpg
:width: 80%
:align: center
```


「Profiles」が表示されない場合  
 - メニューバー上部で右クリック  
 - 「Profiles」に ☑ を入れる  
```{figure} /images/03_workflow_create_profile_profiles_check.jpg
:width: 80%
:align: center
```

**トラブルシューティング**

**＋キーを押してもGalleryにProfileが追加されない場合**  \
＋キーを押してもGalleryにProfileが追加されない場合  
Galleryの表示ウィンドウが小さいケースが考えられます。
```{figure} /images/03_workflow_create_profile_gallery_window.jpg
:width: 80%
:align: center
```

その場合、Galleryウィンドウの◀&rarr;をクリックすると追加したProfileが表示されます。
```{figure} /images/03_workflow_create_profile_gallery_window_adjustment.jpg
:width: 80%
:align: center
```

```{note}
FCSでは同一フレームのProfileは重複して追加されないようになっています。  
重複した場合、Logウィンドウで  
WARNIG:Frame ○○ already has a Profile associated with it  
と表示されます。  
```
```{figure} /images/03_workflow_create_profile_warnig_profile.jpg
:width: 80%
:align: center
```
