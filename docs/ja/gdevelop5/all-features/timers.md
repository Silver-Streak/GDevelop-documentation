---
title: タイマー
---
# タイマー

###  シーンタイマー 

条件とアクションを使うと**シーン**タイマーを起動できます。そしてタイマーが特定の時間になったらアクションを実行することができます。
おそらく最もよく目にするイディオムは、条件でタイマーの経過時間を比較し、アクションでタイマーを 0 にリセットするという組み合わせでしょう。使う前には常にタイマーをリセットすることを推奨します。もし条件やアクションが存在しないタイマーを参照した場合、それは自動的にメモリー上に作成されます。

タイマーには自由に名前をつけられます。_タイマーの名前はテキスト/文字列式のため、二重引用符で括る必要があります。_

もう少し高度なタイマーの例を挙げましょう。タイマーを使ってプレイヤーをダメージから短時間守ります。無敵時間の長さは `player_undestroyable_time` 変数に設定されています。

![](/gdevelop5/all-features/timer-and-variable.png)

!!! tip
    
        **やってみよう！** 🎮  
    次のサンプルをオンラインで実行してみましょう：https://editor.gdevelop-app.com?project=example://asteroids

## オブジェクトタイマー

シーンだけでなく、ゲームオブジェクトとそのインスタンスにもタイマーがあります。オブジェクトの各インスタンスごとに、専用のタイマーがメモリー上に保持されます。他のインスタンスとの共用ではない、独立した個別タイマーです。この機能を使うと、あるオブジェクトのインスタンスアクションを X 秒おきに実行するというようなことができます。

オブジェクトタイマーはシーンタイマーと同じ手順で設定します。［タイマーをスタート（またはリセット）］アクションでオブジェクトのインスタンスタイマーを初期化します。

![](/gdevelop5/all-features/start-object-timer.png)

シーンタイマーと同様に、オブジェクトタイマーの名前もテキスト/文字列式になります。//二重引用符で括ってください。//
上図のアクションはスプライトオブジェクトの各インスタンスごとに "`color`" という名前のタイマーを作成し、それをスタートします。

今度はタイマーの値をチェックしてみましょう。

![](/gdevelop5/all-features/object-timers.png)

上図の条件は "`color`" タイマーの経過時間がオブジェクト変数よりも大きいかどうかをチェックします（式を使ってオブジェクト変数の値を取得できます）。その結果、オブジェクト変数 "`color_time`" よりも経過時間の大きいタイマー値を持つすべてのスプライトインスタンスが選択されます。それからスプライトの色をランダムな色に変更し、オブジェクトタイマーをリセットします。

オブジェクト変数を使ってオブジェクトタイマーをチェックするのは便利です。たとえば敵のインスタンスが複数あり、それぞれオブジェクトタイマーを使って異なる間隔で銃を撃ってくるものとします。"`発砲間隔`" 変数とタイマー値を比較して、タイマーが大きければ発砲する仕組みです。ここで、ある敵が「銃パワーアップ」アイテムに接触したとしましょう。その敵の "`発砲間隔`" 変数の値を通常より小さく変更すると、それだけで前より短い間隔で攻撃してくるようになります。

!!! tip
    
        **やってみよう！** 🎮  
    次のサンプルをオンラインで実行してみましょう：https://editor.gdevelop-app.com?project=example://objects-timers

![](/gdevelop5/all-features/fireratetimerexamplenew.png)

## 高度な話題：変数でタイマーをシミュレートする

シーンタイマーとオブジェクトタイマーは便利です。しかしときには、変数でタイマーをシミュレートする必要が発生するかもしれません。複雑なタスクの場合は、ありえます。この方法は、タイマーを使うよりも柔軟性があります。変数を使うと、値を増やすだけでなく、減らすこともできます。//もしシーンにあるオブジェクトの全インスタンスについて個別にタイマーを持たせたいなら、`TimeDelta` 式と一緒に変数を使うといいでしょう//。

![](/gdevelop5/all-features/increase-variable-timer.png)

上のユースケースでは、1 秒あたり 1000 単位の速度を変数に加算しています。1 秒あたり 1000 単位ということは、この「タイマー」はミリ秒相当の分解能になります。

次の例では、変数（Damage Timer）と比較して 0.5 秒後であればアクションを実行し、そのあと「タイマー」をリセットしています。

![](/gdevelop5/all-features/reset-variable-timer.png)