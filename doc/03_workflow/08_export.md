## エクスポート

FCSでは作業したセッションを出力することができます。

主に以下の際にご活用いただけます。

- FCSのセッションをアーカイブ化や共有する際、キャッシュなどの共有に必要ないデータを除いて手早く共有する
- 同じアクターのProfileから、別のキャラクターの表情を制作する
- 同じキャラクターの表情を、別アクターで制作する

---
```{rubric} **エクスポート手順**
```

1. 出力したいセッションをロード

<br>

2. File/SessionからExportを選択

```{figure} /images/03_workflow_export_menu_bar.jpg
:width: 80%
:align: center
```

<br><br>

3. 出力先をプロジェクトフォルダーとして指定

```{figure} /images/03_workflow_export_export_window.jpg
:width: 80%
:align: center
```

<br>

<!--start_here-->

**①Project Folder**：出力先を指定  

**②Actor**：アクター名を指定　　※アーカイブ化の場合はそのままでも問題ありません  

**③Character**：キャラクター名を指定　　※アーカイブ化の場合はそのままでも問題ありません  

**④Profile**: 現在のセッションのプロファイルを出力するかどうかを指定  

**⑤Videos**: 出力先にビデオデータをコピーするかを指定  
　・ No video：動画データをコピーしない  
　・ Associated video：関連する動画のみコピー  
　・ All files：Recdata内のすべての動画データをコピー  

**⑥Facial/Assets Folder**: 出力先にFacial/Assetsのフォルダーをコピーするかを指定  

<br>

```{note}
Project Folderの項目ではエクスポート先のプロジェクトフォルダのパスを指定します。  
このときプロジェクトフォルダ以下のフォルダ構造が存在しない場合は新しくフォルダが作成されるので、  
例えばE:\test\FCS\testActor\testCharacterと同じ階層にtestCharacter2をエクスポートしたい場合には  
Project Folderの項目に「E:\test」を指定し、Characterの項目に「testCharacter2」と入れてください。
```

<!--end_here-->

<br>

4. Exportボタンを押して出力
   
<br>

---
