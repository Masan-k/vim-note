# vim
インデントでフォーマット
```
:set foldmethod=indent
:set foldlevel=1        " レベル1まで開く（それ以上は折りたたみ）
```
マニュアル時にカッコ（{ と }）を基準に範囲を折りたたむコマンド
```
zfa}
````
ウィンドウの切り替え
```
Ctrl + w + w
```
取り消しの取り消し
```
Ctrl + r
```
Undolistの表示(プラグイン)
```
:UndotreeToggle
```

置換
```
:%s/foo/bar/gc
```

折りたたみを保存
```
:mkview
```
保存した折りたたみを読み込み
```
:loadview
```

特定範囲の行の行頭だけに、文字を挿入したいときは次のようにします。
```
0 で行頭にフォーカスを移動する。
Ctrl-v で矩形選択モードにし、j を数回押して、対象範囲の行の行頭がすべて選択された状態にする。
Shift-i で行頭への挿入モードに入り、任意の文字を入力。
Esc で挿入モードを抜ける
```

例: Visual mode で選択した部分を折り畳む  
```
1. Visual mode (Shift-v) で領域選択  
2. zf
```  
例: カーソル位置から、指定した文字列が見つかるところまでを折り畳む
```
zf /string
```
一度 zf コマンドによって折りたたんだ領域は、zo で展開、zc で折りたたみを行えるようになります。

折りたたみと展開（カーソル位置の要素に対して）
- zc  -- 折りたたみ (Close one fold under the cursor)
- zo  -- 展開（一段階）(Open one fold under the cursor)
- zO  -- 展開（すべて）(Open all folds under the cursor recursively)

折りたたみと展開（ファイル全体の要素に対して）
- zm -- 折りたたみ（一段階） (Fold more)
- zM -- 折りたたみ（すべて） (Close all folds)
- zr -- 展開（一段階） (Reduce folding)
- zR -- 展開（すべて） (Open all folds)

```
:set foldmethod=indent
:set foldmethod=manual
```

```
:tabnew filename.txt
:tabnext または :tn　または gt
:tabclose
:tabonly
```
