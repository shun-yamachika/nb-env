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

# パッケージをインストール
pip install -r requirements.txt
```

## 含まれるパッケージ

主要なパッケージ：
- netsquid
- numpy
- pandas
- matplotlib
- scipy
