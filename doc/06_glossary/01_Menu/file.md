## File

Fileメニューのうち、Session（セッション）ファイルの新規作成、保存、読み込みなど、プロジェクト管理に関連するメニュー項目について説明します。  
※[File ▶ Settings](settings.md)については別ページを参照ください。  

`````{tab-set}

````{tab-item} File

```{figure} /images/06_glossary_Menu_File.jpg
:width: 80%
:align: center
```

<br>

① Settion：Session(セッション)ファイル関連メニューです。  

② Settings：[Settings](settings.md)参照してください。  

③ Quit：FCSを終了します。  

````

````{tab-item} Session ▶

<br>

Session(セッション)ファイルに関連したメニューです。  
Sessionを開く、設定の変更、新規Sessionの作成などを実行することができます。  

```{figure} /images/06_glossary_Menu_File_Session.jpg
:width: 80%
:align: center
```

<br>

① New：Sessionを新規で作成します。   
　「Create new Session」ウィンドウを開きます。  

② Open：Sessionを開きます。  
　・Open...：ダイアログから.yamlファイルを選択してSessionを開きます。  
　・「パス」：最近使用したSessionのパスが表示されます。  

③ Info：Sessionに関する情報を確認できます。  
　「Session Data」ウィンドウが開きます。  

④ Export：Sessionをエクスポートするための「Export Session」ウィンドウが開きます。  

````


````{tab-item} Create new Session

<br>

・Session ▶ New  
　Sessionを新規作成する際に開かれるウィンドウです。  

```{figure} /images/03_workflow_session_create_name.jpg
:width: 80%
:align: center
```

<br>

① Project Folder：FCSの作業データを置きたい場所を指定してください。  
　【Browse...】：ダイアログを開いてプロジェクトフォルダの作成先を入力します。    
　【Create】：パス入力後、FCSのプロジェクトフォルダを作成します。  

② Actor：モーションキャプチャアクター名入力欄です。
　【+】「Create new actor」ウィンドウを起動し、アクター名のフォルダを作成します。  
　　アクター名はプルダウンに追加されます。  

③ Character：3Dモデルのキャラクター名入力欄です。  
　【+】「Create new character folder」ウィンドウを起動し、キャラクター名のフォルダを作成します。  
　　キャラクター名はプルダウンに追加されます。  

④ Maya Scene：3DモデルのMayaシーンへのパスを指定してください。    
　【Browse...】：ダイアログを開いてパスを入力します。    

⑤ Maya Base：「workspace.mel」があるフォルダのパスを入力してください。  
　【Browse...】：ダイアログを開いてパスを入力します。    

⑥ Maya Ver：3Dモデルを作成したMayaのバージョンを指定してください。  


<br>

```{rubric} **Create new Sessionで作成されるフォルダ構造**
```

<br>

```{include} ../../03_workflow/02_create-or-open-session.md
    :start-after: <!--start_here-->
    :end-before: <!--end_here-->
```

<br>

````

````{tab-item} Session Data  

・Session ▶ info  
　右クリックメニューから内容のコピーや編集を行うことができます。  

```{figure} 06_glossary_Menu_File_Session_info.jpg
:width: 80%
:align: center
```

<br>

| 項目 | 説明 | 右クリックメニュー| 
|:-------------:|:--------------|:--------------|
|① Project Folder|プロジェクトフォルダのパス|パスのコピー|
|② Actor|アクター名|リネーム・コピー|
|③ Character|キャラクター名|リネーム・コピー |
|④ Maya Scene|Mayaシーンパス| パスのコピー・変更|
|⑤ Maya Base|workspace.melのパス| パスのコピー・変更|
|⑥ Maya version| Mayaバージョン|コピー・変更|
|⑦ Profile Count|セッション内のプロファイルの数|コピー|
|⑧ Video Count|セッションにインポートした動画の数 | コピー|
|⑨ Created at| セッション作成日時| コピー|
|⑩ Created by| セッション作成者| コピー|
|⑪ Last saved at| 最終保存日時| コピー|
|⑫ Last saved by| 最終保存者| コピー|

<br>

````


````{tab-item} Export Session

<br>

・Session ▶ Export  
　作業したSessionを出力することができます。  

Sessionのエクスポートについては[作業フロー/エクスポート](../../03_workflow/08_export.md)を参照ください。

```{figure} /images/03_workflow_export_export_window.jpg
:width: 80%
:align: center
```

<br>


```{include} ../../03_workflow/08_export.md
    :start-after: <!--start_here-->
    :end-before: <!--end_here-->
```

````

`````

<br><br>

**Menu説明 目次**  
```{include} index.md
    :start-after: <!--start_here-->
    :end-before: <!--end_here-->
```
