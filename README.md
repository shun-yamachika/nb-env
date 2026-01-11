# nb-env

Python仮想環境の依存パッケージ管理リポジトリ

## 必要要件

- **Python 3.8.18** (推奨)
- NetSquid 0.7.5とpydynaa 0.2.4はPython 3.8用にビルドされています

## セットアップ方法

別のPCでこの環境を再現するには：

```bash
# Python 3.8.18で仮想環境を作成（pyenvを使用する場合）
~/.pyenv/versions/3.8.18/bin/python -m venv nb-env

# または、システムのPython 3.8を使用
python3.8 -m venv nb-env

# 仮想環境をアクティベート
source nb-env/bin/activate  # Linux/Mac (bash)
source nb-env/bin/activate.fish  # Linux/Mac (fish)
# または
nb-env\Scripts\activate  # Windows

# 方法1: すべてまとめてインストール（NetSquid関連でエラーが出る可能性あり）
pip install -r requirements.txt

# 方法2: NetSquidを別途インストール（推奨）
# まず通常のパッケージをインストール
pip install -r requirements-base.txt

# NetSquidのインストール（NetSquidフォーラムのアカウントが必要）
# https://forum.netsquid.org/ でアカウント作成後、以下を実行
# 注意: requirements-netsquid.txtで指定されたバージョン（0.7.5）をインストールします
pip install -r requirements-netsquid.txt --extra-index-url=https://pypi.netsquid.org

# または、バージョンを明示的に指定してインストール:
# pip install netsquid==0.7.5 pydynaa==0.2.4 cysignals==1.11.4 --extra-index-url=https://pypi.netsquid.org

# 方法3: wheelファイルからインストール（最も簡単・推奨）
# まず通常のパッケージをインストール
pip install -r requirements-base.txt

# NetSquid関連パッケージをwheelファイルからインストール
pip install wheels/netsquid-0.7.5-cp38-cp38-linux_x86_64.whl wheels/pydynaa-0.2.4-cp38-cp38-linux_x86_64.whl
```

### 注意事項
- **NetSquid**はPyPIにない特別なパッケージです
- このリポジトリには **Python 3.8用のwheelファイル** が `wheels/` ディレクトリに含まれています
- wheelファイルからのインストール（方法3）が最も簡単で推奨されます
- NetSquidフォーラムのアカウントがある場合は方法2も使用可能です

## 含まれるパッケージ

主要なパッケージ：
- netsquid
- numpy
- pandas
- matplotlib
- scipy
