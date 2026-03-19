## Contorollerの登録

Window&rarr;ControllerでConrollerウィンドウが起動します。  
Contollerウィンドウでは、接続しているMayaSceneのコントローラーリグを登録することができます。

<!-- コントローラーウィンドウ画像　取り直す -->
```{list-table}
:widths: 40 60
:header-rows: 0

* - ![](/images/03_workflow_register_controller_window_controller.jpg)
  - Window&rarr;ControllerでConrollerウィンドウが起動します
```

```{note}
コントローラーウィンドウについての説明は[ユーザーガイド/Menu/Window/controller](../06_glossary/01_Menu/window)をご覧ください。
```

<br>

```{rubric} **Region（リージョン）とは**
```

FCSでは顔のパーツ区分のことをRegionと呼びます。  


```{note}
 - Upper（アッパー）：眉周りの動きのこと。眉の上下や眉間にしわを寄せる動きなど。  
 - Eyelid（アイリッド）：まぶたの動きのこと。まばたきや目を細める動きなど。  
 - Gaze（ゲイズ）：目線の動きのこと。目線の上下左右や寄り目の動きなど。  
 - Lower（ロウワー）：鼻、頬、口周りの動きのこと。頬や鼻から下の動き全般
```

<br>

アニメーション解析のため、Upper、Eyelid、Gaze、Lowerにそれぞれコントローラーリグを１つ以上登録してください。    

<br>

また、コントローラーリグの登録時にRegionの最大値最小値も登録できます。  
最大値最小値は自動で入力されますが、値があまりにも大きすぎる場合は調整を行って下さい。  
<!-- 画像追加 -->
```{figure} /images/03_workflow_register_controller_min_max.jpg
:width: 80%
:align: center
```
<br>

```{warning}
数値ではない(True/False)アトリビュートがあると正常に動作しないため、登録から除外してください。
```

<br><br>

```{rubric} **Controllerの登録**
```

Upperの登録を例にcontrollerの登録方法を説明します。  

MayaでUpperに登録したいコントローラーを選択
```{figure} /images/03_workflow_register_controller_maya_upper_select.jpg
:width: 80%
:align: center
```

<br>

【Add selected】を押す
```{figure} /images/03_workflow_register_controller_add_selected_uppper.jpg
:width: 80%
:align: center
```

<br>

Mayaで選択したコントローラーが【Controller】に表示されるので、
select All（=全選択）でUpperに登録したいコントローラーを選択  
※null＝Regionが未指定
```{figure} /images/03_workflow_register_controller_select_all_uppper.jpg
:width: 80%
:align: center
```

<br>

今回はUpperに登録したいので 【**Upper**】を選択    
RegionにUpperと表示されたら登録完了です。
```{figure} /images/03_workflow_register_controller_confirmation_uppper.jpg
:width: 80%
:align: center
```

<br>

同じように他のRegion（Eyelid/Gaze/lower）を登録します。  

<br>

**操作性向上に関する変更**  
Mayaでコントローラーを選択して「Add selected」を実行すると、  
選択したコントローラーが「Controller」に自動的に追加され、チェックが入った状態になります。  
```{figure} /images/03_workflow_register_controller_add_selected_improvement.png
:width: 80%
:align: center
```

<br>

同様に別のコントローラーを選択して「Add selected」した例が下図です。  
こちらも自動的にチェックが入ります。  
このように連続して登録する際に、選択したコントローラーが自動で反映されるようになっています。  
```{figure} /images/03_workflow_register_controller_auto_check.png
:width: 80%
:align: center
```

<br>

次に登録したいコントローラーを選択し【Add selected】するとUpperの下に追加したコントローラーが表示されます。  
例として画像では【Eyelid】を選択しています。  
```{figure} /images/03_workflow_register_controller_add_selected_eyelid.jpg
:width: 80%
:align: center
```

<br><br>


 ```{rubric} **Controller　フィルター機能**
```

 - 右上のall▼のタブを選択し、null▼に変更する  
Regionを設定したものを非表示にし、未登録のコントローラーのみ表示させることができます。  
また、Upper/Eyelid/Gaze/Lowerを選択すればそれぞれ登録したRegionで絞り込むこともできます。
```{figure} /images/03_workflow_register_controller_all_null_eyelid.jpg
:width: 80%
:align: center
```

<br>

```{note}
select Allは表示されているもののみ選択します。  
また、Unselect Allで選択解除が可能です。
```

<br>


nullで絞り込んでいるのでこの状態でRegionを登録すると非表示になります。  
allに戻すとすべて表示されます。  
```{list-table}
:widths: 50 50
:header-rows: 0

* - ![](/images/03_workflow_register_controller_all_view.jpg)

    all選択時

  - ![](/images/03_workflow_register_controller_null_view.jpg)

    null選択時
    
```

<br>

Upper/Eyelid/Gaze/Lowerをすべて登録し終えたら 【Save】してください。
```{figure} /images/03_workflow_register_controller_save.jpg
:width: 80%
:align: center
```

<br>

```{warning}
Regionが未登録状態(null)のものがあるとSave出来ません
```

<br><br>

```{rubric} **登録しないコントローラーを削除する方法**
```

 - 削除したいコントローラーを選択(☑) &rarr; Remove
```{figure} /images/03_workflow_register_controller_remove.jpg
:width: 80%
:align: center
```

<br>

 - 【Remove empty】nullのままのコントローラーを一括削除
```{figure} /images/03_workflow_register_controller_remove_empty.jpg
:width: 80%
:align: center
```

<br><br>

```{rubric} **マニュアル以外のコントローラーを登録したい場合**
```
本マニュアルでは、UnrealEngineのMetahumanを使用していますが、別の3DCG作成ソフトで作成したものでも、各部位に連携できるコントローラーリグがあれば対応可能です。  
また、必要最低限のコントローラーのみを登録していますので、任意で登録するコントローラーを増やすことができます。  

<br>

```{rubric} **Add selectでコントローラーの追加ができない場合**
```
```{warning} 
設定したMayaバージョンとsceneを作成したMayaバージョンが一致しているか確認してください。
```

<br>

```{rubric} **コントローラーの登録順番を変えたい場合**
```

例：L/R　blinkが離れていて不便なのでblinkを上下（隣接するよう）に並べたい  
```{list-table}
:widths: 40 60
:header-rows: 0

* - ![](/images/03_workflow_register_controller_Rearrange.jpg)
  - 【Rearrange】に☑を入れる　→  
     並び替えたいコントローラーをドラッグしドロップ  
     で順番を変更できます。  
```

<br>

**コントローラーの登録順を戻したい場合**
```{list-table}
:widths: 40 60
:header-rows: 0

* - ![](/images/03_workflow_register_controller_reset.jpg)
  - Reset → controller info登録時の順番に戻ります。  
```

<br>

作業しやすいように並び替えたら必ず【Save】してください。
```{figure} /images/03_workflow_register_controller_save.jpg
:width: 80%
:align: center
```

<br>
