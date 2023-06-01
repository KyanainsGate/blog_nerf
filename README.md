# NeRF再現実装公開用リポジトリ
[三次元空間のニューラルな表現とNeRF](https://blog.albert2005.co.jp/2020/05/08/nerf/)で使用したプログラムです．

## 実行方法
- `requirements.txt` に書かれているライブラリをインストールしてください．バージョンは厳密に合わせなくてもだいたい動きます．
- あとはノートブックを上から順に実行していくだけ．

## 元論文
NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis
- arXiv: https://arxiv.org/abs/2003.08934
- プロジェクトページ: http://www.matthewtancik.com/nerfhttp://www.matthewtancik.com/nerf

## Create new kernel
Install PyTorch (See release notes from [here](https://pytorch.org/get-started/previous-versions/) for the detail) and create the Jupyter kernel

```shell
conda create -n bnerf python=3.9
# CUDA 11.3
pip install torch==1.12.1+cu113 torchvision==0.13.1+cu113 torchaudio==0.12.1 --extra-index-url https://download.pytorch.org/whl/cu113
pip install -r requirements.txt
ipython kernel install --user --name=bnerf --display-name=bnerf
```

Set `[Kernel] -> [Change Kernel] -> [bnerf]`  after running `jupyter notebook` in your terminal