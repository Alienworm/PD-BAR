# PD-BA&R
## 1. Requirements
- Python 3.7
- torch 1.13.1+cu171
- torch_geometric 2.2.0
- numpy 1.21.6
- pandas 1.1.5
- sqlite3 2.6.0
## 2. Datasets
- raw_data/Steam
- raw_data/Youshu
- raw_data/NetEase
## 3. Scripts
- get_args.py: parse arguments(with default values) from command line
- run.sh: run the model with specified arguments
## 4. Example of running the model on Steam dataset
```python
./run.sh --dataset_name Steam --tr "(8,20)" --ars "[(7,7)]" --an 2 --max_sample_num_per_user 1 --augment_batch_size 256 --train_batch_size 256 --max_ub_num_quantile 1.0 --max_ui_num_quantile 1.0 --max_bi_num_quantile 1.0 --early_stop 20 --embedding_dim 64 --eval_interval 5 --lightgcn_layers 5 --noise_scale 0.2
```