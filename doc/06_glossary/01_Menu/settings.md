## 環境設定（File ▶ Settingsウィンドウ）

Fileメニューのうち、FCSの全体的な動作環境やパス設定、および詳細なカスタマイズを行うための設定メニューについて解説します。  

```{figure} /images/06_glossary_Menu_Settings.jpg
:width: 80%
:align: center
```

`````{tab-set}

````{tab-item} UI


```{figure} /images/06_glossary_Menu_Info.jpg
:width: 80%
:align: center
```

<br>

① Global  
 a.Font Size：文字の大きさ  
 b.Language：言語設定  

② Gallery  
 a.Thumbnail width：ギャラリーに表示されるプロファイル画像の横幅  
 b.Default Cols：ギャラリーのデフォルトの列数  

③ Video Player  
 a.Cache Frame Max：メモリにキャッシュするフレームの最大値  
 b.Default Tags：デフォルトで付与するタグ名  

<br>

```{note}
Cache Frame Maxは数値を上げるほど多くのメモリ容量を消費します。  
FullHDサイズだと10000fごとに約64GB使用される目安です。  
-1を指定すると無制限にキャッシュを保存します。  
この設定は十分なメモリがある場合のみ使用してください。
```
<br>

④ Video Library  
 a.Cache Frame Max：Videoインポートで回転処理の設定画面を表示するかどうか  
 b.Default Rotation：Videoインポート時のデフォルトの回転値（0＝回転なし）  

````



````{tab-item} Output

- Default output options \
Default Folder \
Default Filename \
Default Filename (Batch) \
Default Maya scene format

- Playblast \
Encoder \
Width \
Height \
Quality \
Percent


````



````{tab-item} Keyboard Shortcuts

- Timeline

| Timeline | Key | Modifier1 | Modifier2 |
|:-------------|:--------------|:--------------|:--------------:|
| Next Frame | Period | Alt |   |
| Previous Frame | Comma |  Alt  |   |
| Next ROM | Period |     |   |
| Previous ROM | Comma |     |   |
| Play/Pause Timeline | V | Alt  |   |
| Add current frame to ROM | Q |     |   |
| Open profile on timeline | E |     |   |

- Editor

| Editor | Key | Modifier1 | Modifier2 |
|:-------------|:--------------|:--------------|:--------------:|
| Save ROM edits | S | Control |   |
| From Maya | V |  Control  |   |
| To Maya | C |  Control  |   |

- Layout

| Layout | Key | Modifier1 | Modifier2 |
|:-------------|:--------------|:--------------|:--------------:|
| Activate Pickup | 1 | Control |   |
| Activate Process | 2 |  Control  |   |
| Activate Register | 3 |  Control  |   |
| Activate Retarget | 4 |  Control  |   |


````



````{tab-item} Maya

CommandPort \
SliderSyncPort \
Open maya scene at launch \
Use gallery character preview \
Image Plane \
Camera \
Install path

````



````{tab-item} Misc

Keep max N video in memory \
Backend \
Update Channel \
Use Beta

Save, Restore, Import

````


`````

<br><br>

**Menu説明 目次**  
```{include} index.md
    :start-after: <!--start_here-->
    :end-before: <!--end_here-->
```



