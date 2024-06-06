## Dataset Collection

1. Vietnamese Wikipedia 
- Get [Vietnamese wikipedia data](https://dumps.wikimedia.org/viwiki/)
- Follow [this repository](https://github.com/namngduc/Word2vec-viwiki) instruction to pre-proccess data and save it as `datatrain.txt`


2. News corpus
- Get `bkai-foundation-models/BKAINewsCorpus` using `load_dataset()` (updated till 2023)
or [@binhvq news corpus dataset](https://github.com/binhvq/news-corpus) (updated till 2019)

Change the pretrain/preprocess.py with the correct text file. 
If you are using news-corpus.txt, just change in line 53:
```python
bkai_dataset = load_dataset("bkai-foundation-models/BKAINewsCorpus", split="train")
```
to 

```python
bkai_dataset = load_dataset("text", "news-corpus.txt", split="train")
```