# CIHGCL: Collective-Individual Intent-Aware Heterogeneous Graph Contrastive Learning for Recommendation

We will organize the complete code and upload it after the paper is accepted for publication.
### Enviroments
- python==3.10
- pytorch==2.0
- cuda==118
- dgl==2.0
## How to Run the code
### Environment Installation
```
pip install torch==2.0 torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```
```
pip install  dgl==2.0 -f https://data.dgl.ai/wheels/cu118/repo.html
```
### Running on Yelp, DoubanBook, Amazon, Movielens and DoubanMovie Datasets
```
python main_CIHGCL.py --model=CIHGCL --dataset=Yelp --gpu=0  --lr=0.0005 --dim=128 --epochs=100 --verbose=1 --GCNLayer=2 --n_intents=32 --intra_ssl_reg=0.05  --cen_reg=1e-5  --cl_rate=0.01  --gamma=1.0 --beta=1.0
```
```
python main_CIHGCL.py --model=CIHGCL --dataset=DoubanBook --gpu=0 --lr=0.0005 --dim=128 --epochs=100 --verbose=1 --GCNLayer=1 --n_intents=64 --intra_ssl_reg=0.1 --cen_reg=1e-5 --cl_rate=0.1 --gamma=1.0 --beta=1.0
```
``` 
python main_CIHGCL.py --model=CIHGCL --dataset=Amazon --gpu=0 --lr=0.0005 --dim=128 --epochs=100 --verbose=1 --GCNLayer=1 --n_intents=64 --intra_ssl_reg=0.05 --cen_reg=1e-5  --cl_rate=0.01 --gamma=1.0 --beta=1.0
```
``` 
python main_CIHGCL.py --model=CIHGCL --dataset=Movielens --gpu=0 --lr=0.0005 --dim=128 --epochs=150  --verbose=1 --GCNLayer=2 --n_intents=64 --intra_ssl_reg=0.05 --cen_reg=1e-4 --cl_rate=0.01 --gamma=1.0 --beta=1.0
```
``` 
python main_CIHGCL.py --model=CIHGCL --dataset=DoubanMovie --gpu=0 --lr=0.0005 --dim=128 --epochs=100 --verbose=1 --GCNLayer=1 --n_intents=64 --intra_ssl_reg=0.1 --cen_reg=1e-5 --cl_rate=0.2 --gamma=1.0 --beta=1.0
```