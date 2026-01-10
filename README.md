# nb-env

Python仮想環境の依存パッケージ管理リポジトリ

## セットアップ方法

別のPCでこの環境を再現するには：

```bash
# 仮想環境を作成
python3 -m venv nb-env

# 仮想環境をアクティベート
source nb-env/bin/activate  # Linux/Mac
# または
nb-env\Scripts\activate  # Windows

# 方法1: すべてまとめてインストール（NetSquid関連でエラーが出る可能性あり）
pip install -r requirements.txt

# 方法2: NetSquidを別途インストール（推奨）
# まず通常のパッケージをインストール
pip install -r requirements-base.txt

# NetSquidのインストール（NetSquidフォーラムのアカウントが必要）
# https://forum.netsquid.org/ でアカウント作成後、以下を実行
pip install -r requirements-netsquid.txt --extra-index-url=https://pypi.netsquid.org
```

### 注意事項
- **NetSquid**はPyPIにない特別なパッケージです
- NetSquidをインストールするには[NetSquidフォーラム](https://forum.netsquid.org/)のアカウントが必要です
- アカウント作成後、`--extra-index-url`オプションを使用してインストールします

## 含まれるパッケージ

主要なパッケージ：
- netsquid
- numpy
- pandas
- matplotlib
- scipy
