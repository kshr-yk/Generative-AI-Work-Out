# Generative-AI-Work-Out
画像生成ワークアウト
1. GAN (Generative Adversarial Network) を使ってみる
環境Google Colab(https://colab.research.google.com/drive/123oD0qBLgP0fQBsuRiZVNIumZOzYjlrw?authuser=0#scrollTo=03CCx54Yc0Qu)

## GAN（特に DCGAN）の基本的な流れ
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