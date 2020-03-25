CityscapesデータセットのTraning画像50枚に対して、ADE20Kの6クラス分のアノテーションを追加したGround Truth画像です。
ランダムで選出したため追加クラスがない画像もあります（追加クラスがある画像はファイル名に_annotatedが含まれています）。

元画像などは以下のパスに入ってます：
/work/mahmuds/Dataset/Cityscapes_Dataset/cityscapes
leftImg8bitが元画像、gtFineがGround Truthです。

追加したクラスは：
- signboard（交通標識や看板など）
- awning（テラス席用の日除けなど）
- bag（手提げバッグ，リュックサックなど）
- trade（店の名前が書かれているプレート）
- flag（旗）
- ashcan（ゴミ箱）

Cityscapesの各クラス定義：
https://github.com/mcordts/cityscapesScripts/blob/master/cityscapesscripts/helpers/labels.py

ADE20Kの150クラス定義：
https://github.com/CSAILVision/sceneparsing/blob/master/objectInfo150.csv

ADE20Kのクラス色：
https://github.com/CSAILVision/sceneparsing/tree/master/visualizationCode/color150

追加分のアノテーションはlabelmeで作成し、pythonスクリプトで元のアノテーション画像と合成しました。
アノテーションデータはjson形式で、元画像と同じフォルダに置けばlabelmeで編集できます。
使用したスクリプトは後日こちらのrepoに上げます：
https://github.com/rikaakiba/CityscapesExtended