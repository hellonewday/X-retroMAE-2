# X-DupMAE
Running [RetroMAE v2: Duplex Masked Auto-Encoder For Pre-Training Retrieval-Oriented Language Models](https://arxiv.org/abs/2211.08769) on RoBERTa model.

Clone from [hieudx149](https://github.com/hieudx149) [X-RetroMAE](https://github.com/hieudx149/X-RetroMAE) repository.

**X-DupMAE** tries to modify [RetroMAE v2](https://github.com/staoxiao/RetroMAE) to be compatible with RoBERTa and XLM-RoBERTa, hope this project will help anyone who wants to apply RetroMAE v2 to their own language rather than English.

## Modification 
Compare to [hieudx149](https://github.com/hieudx149) version:
- Clone [RetroMAE v2](https://github.com/staoxiao/RetroMAE) modeling_duplex.py and change all Bert* to Roberta* 
- Clone DupMAECollator to data.py
- Add code to switch between retromae and dupmae in run.py 

## Setup
```
pip install --upgrade pip
pip install -r requirements.txt
```

## Run pretraining
First make sure that you have preprocessed your own data first by running the preprocessing.py in examples/pretrain, then run:
```
sh src/run_pretrain.sh
```

## Citation
```
@inproceedings{RetroMAE,
  title={RetroMAE: Pre-Training Retrieval-oriented Language Models Via Masked Auto-Encoder},
  author={Shitao Xiao, Zheng Liu, Yingxia Shao, Zhao Cao},
  url={https://arxiv.org/abs/2205.12035},
  booktitle ={EMNLP},
  year={2022},
}
```
