
## アニメーションの出力方法

```{caution}
解析する動画が広角レンズを使って撮影されている場合、Solverの設定変更が必要です。  
詳しくは[ユーザーガイド/Menu/Window/Solver](../06_glossary/01_Menu/window)をご確認ください。
```

<br>

```{rubric} **単体のアニメーション出力**
```

```{note}
出力画面の項目についての説明は  
[ユーザーガイド/Menu/Window/Videos 右クリック](../06_glossary/01_Menu/window)をご確認ください。
```

<br>

1.Videosウィンドウで解析/出力したい動画名の上で右クリックします。  
画像のメニューが表示されるので、▼Process を選択・該当する項目に ☑ を入れ、
```{figure} /images/03_workflow_export_animation_process_check.jpg
:width: 80%
:align: center
```

<br><br>

2.【Start process】を押します。  
```{figure} /images/03_workflow_export_animation_start_process.jpg
:width: 80%
:align: center
```

<br>

````{note}
解析結果を見てから再度調整を行いたい場合はPlayblastやSceneの ☑ を外しておくと時間短縮できます。  

```{figure} /images/03_workflow_export_animation_export_options.jpg
:width: 80%
:align: center
```

````

<br>

````{note}
 初回出力時は時間がかかる場合があります。  

```{figure} /images/03_workflow_export_animation_export.jpg
:width: 80%
:align: center
```

````

<br>

3.出力中Mayaシーン上に ☑ を入れた項目が反映されていきます。
   - タイムスライダーに音声データ
   - イメージプレーンに連番画像
   - アニメーションデータ の順で反映される
   - アニメーションデータ反映時はスライダーが動く

```{figure} /images/03_workflow_export_animation_maya_reflection.jpg
:width: 80%
:align: center
```

<br><br>

4.出力完了  
playblastやsceneに ☑ していた場合、  
出力が完了したらエクスプローラーがポップアップします。
```{figure} /images/03_workflow_export_animation_export_complete.jpg
:width: 80%
:align: center
```

<br><br>

```{rubric} **動画の一部範囲のみを再処理して出力**
```

Timelineの一部表示機能を使用して、FCSのTimelineで表示している範囲のみのアニメーションを出力することができます。  
※本機能は **FCS 25.04.02** 以降に搭載されています。  

<br>

1.FCSのTimeline範囲をアニメーション出力したい部分に設定します。
```{figure} /images/03_workflow_export_animation_partial_process.jpg
:width: 80%
:align: center
```

<br><br>

2.Timelineの動画名を右クリックし、【Segment Only】にチェックを入れ、  
【Start processing】を押します。
```{figure} /images/03_workflow_export_animation_partial_process_export.jpg
:width: 80%
:align: center
```

<br>

```{admonition} Maya Start の値について  
 FCSで一部範囲を指定し出力したアニメーションをMayaの指定のフレームに出力できます。  
 <例>
 - FCS Timeline上の指定範囲：100F～200F
 - Maya Start：50  
 →この場合、アニメーションはMayaの『50F～150F』に出力されます。  

<dr>

デフォルトでは『-1』となっており、この場合はFCSで指定した範囲と同じフレームに出力されます。  
例：上記の場合、Mayaでも100F～200Fに出力されます。
```

<br>

````{caution}
Timelineの動画名を右クリックし表示されるメニューからのみ実行可能です。  
（Videosウィンドウからは実行不可）

```{figure} /images/03_workflow_export_animation_partial_process_export02.jpg
:width: 80%
:align: center
```

````

<br>

3.実行結果 指定した範囲のみアニメーションが出力されます。
```{figure} /images/03_workflow_export_animation_partial_process_complete.jpg
:width: 80%
:align: center
```

<br><br>

**ーーーーーここからーーーーーーー**
```{rubric} **複数のアニメーション出力**
```

```{note}
出力画面の項目についての説明は  
[ユーザーガイド/Menu/Window/Processer](../06_glossary/01_Menu/window)をご確認ください。
```

<br>

Videosウィンドウで解析/出力したい動画名の左側の ☑ をつける  
```{figure} /images/03_workflow_export_animation_processor_video_check.jpg
:width: 80%
:align: center
```

<br><br>

Processorウインドウを開く
```{figure} /images/03_workflow_export_animation_window_processor.jpg
:width: 80%
:align: center
```
<br>

```{figure} /images/03_workflow_export_animation_processor_output_name.jpg
:width: 80%
:align: center
```

 - 該当する項目に ☑ を入れ
 - Output Filename を任意の名前に変更
```text
- {solver} → solverの名前
- {video} → ビデオのファイル名
- {user} → windows ユーザ名
- {project} → 案件フォルダ名
- {chara} → キャラクター名
- {actor} → 役者名
- {%Y%m%d}, {%H%M%S} → 年月日、時間分秒

{video}のみにするとimportした動画名で出力される
```
 - Start
```{figure} /images/03_workflow_export_animation_processor_confirm.jpg
:width: 80%
:align: center
```

出力が完了したらエクスプローラーがポップアップします。
```{figure} /images/03_workflow_export_animation_processor_complete.jpg
:width: 80%
:align: center
```
<br>

**カメラ・イメージプレーンについて**  \
Frames、またはLM Framesにチェックを入れた場合、Maya内のイメージプレーンに連番画像がセットされます。  
連番画像をセットしたいカメラ・イメージプレーンの名前を「Settings/Maya/Camera」「Settings/Maya/ImagePlane」から設定してください。

デフォルトの設定は以下の通りです。

- イメージプレーン → imagePlane1
- カメラ → fcs_cam1

指定した名前のカメラ・イメージプレーンがシーン内に無い場合は新しく作成されます。  
パイプラインに合わせてカメラの名前を随時設定してください。

