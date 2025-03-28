# 教師なしドメイン適応における信頼度較正のための生成モデルの導入

このリポジトリは、lhoyer 氏の CVPR 2023 に採択された論文で提案された教師なしドメイン適応の手法を基に、その信頼度を較正するために生成モデルを導入する手法を実装したものです。

## 概要

教師なしドメイン適応 (Unsupervised Domain Adaptation, UDA) は、ラベル付きのソースドメインとラベルなしのターゲットドメイン間で知識を転移する手法です。本リポジトリでは、lhoyer 氏の UDA 手法をベースに、信頼度較正を目的として生成モデルを追加することで、適応性能の向上を目指します。

## 特徴
- lhoyer 氏の CVPR 2023 に採択された手法を再現
- 信頼度較正のための生成モデルの追加
- PyTorch による実装

## 環境

本プロジェクトは以下の環境で動作確認を行っています。
- Python 3.8+
- PyTorch 1.10+
- torchvision 0.11+
- その他の依存ライブラリは `requirements.txt` に記載

## インストール

```bash
# リポジトリのクローン
git clone https://github.com/your-repo-url.git
cd your-repo

# 仮想環境の作成（任意）
python -m venv venv
source venv/bin/activate  # Windows の場合: venv\Scripts\activate

# 依存関係のインストール
pip install -r requirements.txt
```

## 使用方法

1. データセットの準備
   - `data/` ディレクトリに配置

2. 訓練の実行
   ```bash
   python train.py --source svhn --target mnist
   ```

3. 評価の実行
   ```bash
   python evaluate.py --target mnist
   ```

## 参考文献

- [L. Hoyer et al., CVPR 2023](https://arxiv.org/abs/xxxx.xxxx)

## ライセンス

本リポジトリのコードは MIT ライセンスのもとで公開されています。

