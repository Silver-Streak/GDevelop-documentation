---
title: 経路探索
---
# 経路探索

**[経路探索ビヘイビアのサンプルがすぐに見たいですか？](#Examples) **

経路探索(パスファインディング)の動作により、オブジェクトを選択した目的地に移動したり、アイテムを障害物としてフラグを立てたりすることができます。障害物としてフラグが付けられているオブジェクトは、移動するオブジェクトによって回避されます。

## オブジェクトにビヘイビアを追加 オブジェクトに動作を追加するには、いつものようにオブジェクトを作成します。次に、シーンインターフェイスの右側にあるオブジェクトリストを右クリックして、オブジェクトのプロパティを開きます。ポップアップリストから\[オブジェクトの編集\]を選択します。

![](/gdevelop5/editplayerobject.jpg)

次に、動作タブを選択し、「動作を追加」ボタンをクリックします。

![](/gdevelop5/behaviors-tab.png)

次に、選択できる2つのオプションがあります。

## オプション１：経路探索の動作 ![](/gdevelop5/behaviors/pathfinding-behavior-inlist.png)

「経路探索(パスファインディング)ビヘイビア」により、障害物としてフラグが立てられているすべてのオブジェクトを回避しながら、オブジェクトを目的地に移動できます。

オブジェクトにビヘイビアを追加した後、いくつかのオプションをカスタマイズできます。 ![](/gdevelop5/behaviors/pathafindin-behavior-options.png)

- **加速度:** オブジェクトがパス上を移動するときに加速する速度です
- **対角線を許可:** オブジェクトが対角線で移動できるかどうかを許可します。
- **角度オフセット:** スプライトが間違った方向を向いている場合、角度オフセットで設定できます。
- **追加境界線サイズ:** オブジェクトの周囲の境界線サイズを設定します。この設定は、オブジェクトが障害物にどれだけ接近できるかを決定します。
- **最大速度:** オブジェクトがパス上を移動できる最大速度。
- **オブジェクトの回転:** パス上を移動中にオブジェクトを回転させたくない場合は、オブジェクトの回転を無効にします。
- **回転速度:** オブジェクトの回転速度を設定します。
- **仮想セルの高さと幅:** パスは仮想グリッドを使用して生成されます。ここでセルのサイズを変更できます。セルのサイズが小さいほど、動きがスムーズになります。セルサイズが小さいほど計算量が多くなるため、サイズをできるだけ大きく保つようにしてください。

## オプション２：経路探索障害動作 ![](/gdevelop5/behaviors/pathfinding-obstacle-inlist.png)

「経路探索(パスファインディング)障害動作」を使用することにより、任意のオブジェクトに障害があるとフラグを立てることができます。オブジェクトに動作を追加した後、カスタマイズする2つのオプションがあります。 ![](/gdevelop5/behaviors/pathfinding-obstacle-options.png)

- **通行不可:** これを有効にすると、障害物は通行不能になります。動いているオブジェクトは、どうにかしてそれを避けようとしています。
- **コスト:** 障害物が通過できない場合、障害物のコストを設定できます。移動するオブジェクトは、目的地への最適な経路を探す際に、コストの高い値の障害物を避けることを好みます。たとえば、川にはコストがかかる場合があります。移動オブジェクトは、可能であれば、それを回避します。ただし、川の周りに他の方法がない場合、または川のコストが他の地域に比べて低い場合、移動オブジェクトは通過します（たとえば、より高いコストで山に登るのではなく）。そして、ワニを川に入れてコストを上げると、動いている物体が代わりに山に登ることを決めるかもしれません。

## サンプル

!!! note
    
        **やってみよう！** 🎮  
    サンプルをオンラインで実行できます

**一般的な経路探索ビヘイビア**

[Open example in GDevelop](https://editor.gdevelop.io/?project=example://pathfinding){ .md-button .md-button--primary }

[![](/gdevelop5/behaviors/pathfindinggeneral.png)](https://editor.gdevelop-app.com/?project=example://pathfinding)

  
**経路探索の基本**

[Open example in GDevelop](https://editor.gdevelop.io/?project=example://pathfinding-basics){ .md-button .md-button--primary }

[![](/gdevelop5/behaviors/pathfindingbasics.png)](https://editor.gdevelop-app.com/?project=example://pathfinding-basics)
