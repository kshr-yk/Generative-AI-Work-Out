# GAN（特に DCGAN）の基本的な流れ
データ準備

画像データを用意し、データローダー（PyTorch の DataLoader など）を作る。
Generator (生成器) と Discriminator (識別器) のモデル定義

Generator: 潜在変数（ノイズベクトル）から画像データを生成するネットワーク
Discriminator: 入力された画像が「本物か／生成画像か」を二値分類するネットワーク
学習ループ

Generator の更新: 生成画像が Discriminator に「本物」と判断されるようにパラメータを調整
Discriminator の更新: 本物画像を「本物」と、生成画像を「偽物」としっかり識別できるようにパラメータを調整
Generator と Discriminator を交互に学習させる
生成結果の可視化

学習の途中経過として、生成された画像を何枚か保存・表示して確認する

## 習得方法
1. 最初は小さいサイズの画像で始める

例: 64×64 程度にリサイズする
計算リソースを抑えつつモデルを試せる
2. ハイパーパラメータやネットワーク構造を色々試す

異なる活性化関数、学習率、バッチサイズ、潜在ベクトルの次元 nz などを変えてみる
3. 学習過程での出力をモニタリング

生成画像がぼやけていたり、崩れたりする場合、過学習やモード崩壊、学習率の問題など色々原因がある
時にはネットワークの初期化や BatchNorm、活性化関数（ReLU, LeakyReLUなど）を見直してみる
4. Kaggle NotebookのGPU活用

Kaggle Notebook を使えば無料でGPUを使って学習可能
大規模データを使う場合は、それでも時間がかかるため、サンプリングやリサイズを上手に使う