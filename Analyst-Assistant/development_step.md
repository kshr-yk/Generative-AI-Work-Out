# 開発の流れ
## Step 1: 簡単なデータ可視化アシスタントを作る
ユーザーがCSVをアップロード
AIがデータを読み取り、特徴を要約
ユーザーの指示に応じて、適切な可視化（ヒストグラム、散布図、折れ線グラフなど）を提案・実行
使用技術:

pandas（データ処理）
matplotlib（可視化）
openai API or llama.cpp（質問応答）
## Step 2: 分析提案の自動化
ユーザーが「このデータで面白い分析をしたい」と言ったら、適切な手法を提案
例: 相関分析、回帰分析、クラスタリング、外れ値検出
使用技術:

scikit-learn（機械学習モデルの提案）
langchain（AIの応答強化）
## Step 3: コード自動生成
「このデータでk-meansクラスタリングをしたい」
AIがPandasやScikit-learnのコードを生成し、実行できるようにする
使用技術:

code-interpreter（Pythonコードの実行）
pandasai（データフレームをAIと連携）