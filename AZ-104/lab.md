# ラボで使用するリージョンについて

japaneast （東日本）は、VMの作成に失敗することがあるようです。

westus2 が安定して使えるようです。

他に westus, eastus などもお試しください。

# 複数行のコマンド貼り付け

複数行のコマンドをコピー・ペーストして実行する際、最終行が貼り付けられただけで実行されない場合があります。貼付け後、Enterキーを押して、最終行も実行されるようにしてください。

# Cloud Shell のタイムアウト

Cloud Shell が 20 分間、操作をしない状態にすると、タイムアウトで切断されてしまいます。

切断されますと、設定されたシェル変数などがクリアされてしまいますので、お気をつけください。

切断されてしまった場合、必要であれば、変数の設定を再度やり直してください。

# Cloud Shellでの貼り付け

Cloud Shellで貼り付けを行う場合は、`Ctrl + Shift + V` を使用してください。

# Cloud Shell 環境へ、ラボのファイルをコピーする

AZ-104のラボ全般で使用されるJSONファイルは、下記の方法で準備すると便利です。

Azure portalでCloud Shell （Bash）を起動し、下記のコマンドを貼り付けます。

```
git clone https://github.com/MicrosoftLearning/AZ-104JA-MicrosoftAzureAdministrator.git
cp `find AZ-104JA-MicrosoftAzureAdministrator/Allfiles/Labs -type f` .
```

コピーされたJSONファイルを確認するには `ls` を使用します。
```
ls
```

あとは、PowerShell に切り替えて、ラボで指示されるように、コマンドを貼り付けていけばOKです。


# Cloud Shell でのファイルの編集について

ファイルを編集する必要がある場合は、Cloud Shellの組み込みのエディターを使用できます。

「{}」ボタン（エディターを開く）で、エディターを起動できます。

エディターを閉じる際は、Cloud Shell右上の「✕」ではなく、「...」アイコンから「エディターを閉じる」、または `Ctrl + Q`で閉じてください。

# ラボ1

タスク2の7でメンバーシップの種類の選択のところがグレーアウトして選択できない場合は、Webブラウザでページをリロードしてください。

最後の「リソースのクリーンアップ」の「8.Azure portal からサインアウトし、サインインし直します。」はなくてもできる場合があります。最初に削除を試してみて、ダメならサインアウト、サインインしてみてください。

# ラボ2a

クリーンアップのコマンドでは、
'[id]' ではなく 'id' と書いてください。

# ラボ2b

# ラボ3a

演習 1
タスク 1: リソース グループを作成し、リソース グループにリソースをデプロイする

3 リージョン このラボで使用するサブスクリプションで使用できる Azure リージョンの名前
westus2（米国西部2）を使ってください。

# ラボ3b

演習 1
タスク 2: ARM テンプレートを使用して Azure マネージド ディスクを作成する

3「テンプレートの編集」 ブレードで、「ファイルの読み込み」 をクリックし、前の手順でダウンロードしたテンプレート ファイルをアップロードします。

は、自分でダウンロードしたものではなく、\Allfiles\Labs\03\az104-03b-md-template.json および \Allfiles\Labs\03\az104-03b-md-parameters.jsonを使ってください。

タスク 2: ARM テンプレートを使用して Azure マネージド ディスクを作成する

８．「カスタムデプロイ」 ブレードに戻って、次の設定を指定します。
のLocationはeastusになりますが、そのまま進めて大丈夫です。

# ラボ3c

ラボ3cとラボ3dは同じ内容で、PowerShellでやるかAz CLIでやるかの違いだけです。どちらか片方を実施いただければ十分です。

# ラボ3d

3dの最後のコマンドがラボ3で使ったリソースの削除コマンドになっています。よって、3cで終わるとリソースがすべて残ります。終わった方は3dの最後のコマンドでリソースグループすべて削除してください。

# ラボ4

【タスク02】（手順3）・jsonファイルを１個ずつアップロードしました。ドラッグして複数ファイルを同時にアップロードはできません。

・２つのファイルがアップロードできているかどうか、確認しましょう。lsコマンドで確認します。

（全体）「ipconfig1」の設定など［保存］することを忘れずに。

【タスク04】（手順4）「ネットワークセキュリティグループ」と「ネットワークセキュリティグループ（クラシック）」があり、見間違えないようにしましょう。「ネットワークセキュリティグループ」で実施できました。

（手順7）「受信セキュリティルール」とありますが、画面では「受信セキュリティ規則」です。

【タスク05】（手順7）反映まで時間がかかりました。数分待ってからページ更新。

# ラボ5

【タスク01】(手順5)「可用性ゾーンに対応したAzureリージョンの名前」は west usにしました。

（手順09）こちらの「可用性ゾーンに対応したAzureリージョンの名前」は　east usにしました。

【タスク02】（手順5）この表だけではなく、これ以降の表についても、設定名と画面表示が異なります。表の上４行が画面では下方に、表の下４行が画面では上方にというイメージです。

例えば、「az104-05-vnet0からリモート仮想ネットワークへのピアリングの名前」は
「リモート仮想ネットワーク」項目の「ピアリング名」で読み替えてください。

# ラボ6
【タスク01】（手順1）east usにしました。

【タスク02】（手順5)ラボ05と同じように、表と画面表示の上下が逆です、ご注意ください。

【タスク03】（手順5)かなり時間がかかりました。１回目はダメで、しばらく経った２回目でＯＫ。

（手順9）「到達不能」ではなく、「到達不可能」と表示されます。

【タスク04】（手順11）ルートテーブルの作成において、「仮想ネットワークを作成したときと同じAzureリージョン」ですが、注意してください。既定値が米国西部2になっています。私はタスク01で米国東部を選んでので、選ぶ直すことになりました。

（手順13・15）「ルート」「サブネット」は”設定”にあります。
【タスク05】（手順9）「暗黙的なアウトバウンド規則の設定」は、「はい」では無く、「推奨」でうまくいきました。
