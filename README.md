reactとreact nativeを共存させて開発を高速でできるようにする試み

## ざっくりとした構成

### react
自前でwebpackを設定する方針
UI周りはMaterial UIかIonic（v4が出れば）

### react native
Expo.ioを採用
ブラックボックスな部分は増えるが一切ネイティブ部分に触れずに開発ができる

### common
reactとreact nativeで共通する処理を含める
主にredux周りの処理がここに入ることになりそう

## 統制

今の所、各パッケージ（reactとreact native）それぞれでtslintの設定を行っている

`lerna run :commmand`で各パッケージ内で該当するscriptを実行できる

commonはどのtslintで直すかは考えどころ（common内にもpackage.jsonを置く？）


## その他

秩序の保ち方に提案があればぜひPR送ってほしい...！
