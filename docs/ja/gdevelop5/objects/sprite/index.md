---
title: スプライトオブジェクト
---
# スプライトオブジェクト

!!! tip
    
        **やってみよう！** 🎮  
    [説明はいいから、とにかく Sprite オブジェクトが動くところを見たい？　わかりました、こちらを先にどうぞ。](/#サンプル)
    

スプライトオブジェクトは、GDevelop で最もよく使用されるオブジェクトです。

スプライトオブジェクトを使うと、画像を表示したり、一連の画像をアニメーションとして再生できます。ボタン、キャラクター、プラットフォーム など、ゲーム内の利用範囲は多岐にわたります。画像で表現できるものはすべて、スプライトオブジェクトにすることが可能です。 

## スプライトオブジェクトを作成する

シーンにスプライトを追加するには、オブジェクトリストの右下にある「クリックしてオブジェクトを追加」オプションを選択します。 

![](/gdevelop5/objects/clicktoaddanobject.png)

新しいパネルが開き、GDevelop で使用可能なさまざまなタイプのオブジェクトが表示されます。 

![](/gdevelop5/tutorials/platform-game/gd5_object_types1.png)

一覧から「スプライト」を選択して、ゲームシーンに新しいスプライトオブジェクトを作成します。 

![](/gdevelop5/objects/select-sprite.png)

オブジェクトを作成すると、プロパティウィンドウが開きます。このウィンドウには、スプライトオブジェクトのプロパティが表示されています。

![](/gdevelop5/objects/sprite-object-properties.png)

## アニメーションを追加する

アニメーションを使用すると、1 つまたは一連の画像をスプライトオブジェクトに追加できます。アニメーションを追加するには、アニメーションの追加ボタンをクリックします。

![](/gdevelop5/objects/add-animation-button.png)

現在のダイアログボックスが展開し、設定可能なさまざまなオプションが表示されます。

![](/gdevelop5/objects/animation-properties.png)

### アニメーションに画像を追加する

「＋」記号をクリックして、オブジェクトのアニメーションに画像を追加できます。

![](/gdevelop5/objects/add-symbol.png)

クリックすると［ファイルを開く］ダイアログが表示され、アニメーション用の画像ファイルを選択できます。画像を選択すると、ウィンドウに画像が表示されます。

![](/gdevelop5/objects/add-image.png)

### 当たり判定とポイント

ダイアログの下部にある［当たり判定を編集］を使用して、スプライトの衝突領域、つまり当たり判定に考慮される領域をカスタマイズできます。くわしくは、[衝突マスクについて](/ja/gdevelop5/objects/sprite/collision-mask)を参照してください。

スプライトプロパティダイアログの下部にある［当たり判定を編集］オプションの隣には、［ポイントを編集］オプションがあります。このオプションを使用すると、オブジェクトの参照ポイントを追加できます。これらの参照ポイントは、必要なときにイベントで使用できます。くわしくは、[スプライトのポイントについて](/ja/gdevelop5/objects/sprite/edit-points)を参照してください。

### 複数のアニメーションを追加する

オブジェクトには、複数のアニメーションが必要な場合があります。アニメーションを追加するには、初回の追加時と同じように［アニメーションを追加］ボタンをクリックします。この機能により、さまざまなアニメーションを簡単に分割管理できます。 

![](/gdevelop5/objects/multiple_animations.png)

イベントを使用して、これらのアニメーションを切り替えることができます。

### アニメーションに名前を付ける

ウィンドウのアニメーションセクションの上部にある「Animation #」の横に、グレーアウトした「アニメーションの別名」フィールドが表示されています。このフィールドをクリックすると、アニメーションの名前を入力できるようになります。 

![](/gdevelop5/objects/name-animation.png)

!!! tip
    
        オブジェクトが複数のアニメーションを持つ場合、アニメーションに名前がないと区別しにくい状態になります。複数のアニメーションを持つオブジェクトには、アニメーション名を使用することをお勧めします。
    
    名前を入力しない場合は、アニメーション番号を使用してアニメーションを参照する必要があります。

### アニメーションに複数の画像を追加する

アニメーションに複数の画像を追加するには、［ファイルを開く］ダイアログから必要なすべての画像を選択して、アニメーションに追加します。

![](/gdevelop5/objects/animation-multiple-images.png)

画像は表示と同じ順序で再生されます。

### アニメーションを繰り返す

デフォルトでは、すべてのアニメーションは 1 回だけ再生されます。つまり最後のフレームが終了すると、アニメーションはすぐに停止します。アニメーション を繰り返したい場合は、［ループ］にチェックを入れて、アニメーションを「ループ」するように設定します。

![](/gdevelop5/objects/set-animation-loop.png)

この設定を行った後は、アニメーションが連続して再生されるようになります。 

### アニメーション時間を設定する

アニメーションの速度は、時計アイコンの値を変更することで設定できます。 

![](/gdevelop5/objects/set-animation-speed.png)

フィールドに入力するのは、2 つの連続するフレーム間の経過時間です。デフォルト値は 0.08 秒です。短いアニメーション時間を設定すると再生が速くなり、長いアニメーション時間を設定すると再生が遅くなります。

## オブジェクトへの名前付け

ダイアログ上部の［オブジェクト名］フィールドにオブジェクトの名前が表示されます。オブジェクトの名前は通常、オブジェクトの内容を表すように設定し、他のスプライトと区別しやすくします。

![](/gdevelop5/objects/annotation_2019-06-09_152442.png)

## シーンにオブジェクトを追加する

新しいスプライトオブジェクトを準備できたら、次はそのインスタンスを目的のシーンに追加する番です。

方法はいくつかありますが、一般的なのは［オブジェクト］リストから配置したいスプライトをシーン内にドラッグする方法でしょう。ドロップした場所に新しいインスタンスが追加されます。他の方法としては、［オブジェクト］リスト上で配置したいスプライトを選択状態にしておき、シーン内で右クリックします。コンテキストメニューが表示されるので、［＜オブジェクト＞のインスタンスを追加］を選択するとインスタンスがシーンに追加されます。スプライトの「インスタンス」は必要な数だけシーンに追加できます。上記の方法を繰り返してもいいですし、配置済みのインスタンスをコピーして貼り付けでも追加できます。 

![](/gdevelop5/objects/addspritetoscene.gif)

## イベントで複数のアニメーションを使いわける

それぞれ独自の画像セットを持つ複数のアニメーションを作成した後、イベントを使用してアニメーションを切り替えることができます。アニメーション時間を 0〜1 に設定すると、イベントを使用するときにアクティブになります。 

!!! note
    
        マイナスのアニメーション時間を使用すると、イベントアクションが無効になります。
    
    //マイナスの値は使用しないでください。// 

オブジェクトに複数のアニメーションを設定した場合、イベントの「名前でアニメーションを変更する」アクションを使って任意のアニメーションを設定できます。このアクションと条件を組み合わせることによって、希望のタイミングで任意のアニメーションに切り替えることができます。 

![](/gdevelop5/objects/eventanimationexample.png)

前述しましたが、複数のアニメーションを簡単に区別できるように、ここではオブジェクト内のアニメーションに名前が付けられているものとします。 

アニメーション名を使用してアニメーションを変更するには、「名前でアニメーションを変更する」アクションを選択します。 

そして「アニメーションの名前」フィールドに引用符で括った名前を指定します。

![](/gdevelop5/objects/eventanimnameexample.png)

イベントの詳細については[チュートリアル](/ja/gdevelop5/tutorials)を参照してください。

## サンプル 

!!! tip
    
        **やってみよう！** 🎮  
    画像をクリックすると、オンラインでサンプルを実行できます。

[![](/gdevelop5/objects/createaspritenew.png)](https://editor.gdevelop-app.com/?project=example://change-scale-of-sprites)

----

[![](/gdevelop5/objects/changespriteanimationexamplenew.png)](https://editor.gdevelop-app.com/?project=example://change-sprite-animation)

----

[![](/gdevelop5/objects/changespritecolorexamplenew.png)](https://editor.gdevelop-app.com/?project=example://change-sprite-color)

----

[![](/gdevelop5/objects/changespriteanimationexample2new.png)](https://editor.gdevelop-app.com/?project=example://play-stop-sprite-animation)