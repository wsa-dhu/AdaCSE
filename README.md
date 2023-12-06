# AdaCSE
### Training
For each existing model to be improved, the samples that the model has difficulty recognizing are first selected as training data from `source data/chatgpt_pair.txt` or `source data/llama_pair.txt` and saved in  `. /data`.
### Training scripts
We provide training scripts `./run.sh`. Training scripts call `./train.py` for training. The script runs with the following code,
```python
bash run.sh
```
### Evaluation
Our evaluation code for sentence embeddings is based on a modified version of [SentEval](https://github.com/facebookresearch/SentEval). It evaluates sentence embeddings on semantic textual similarity (STS) tasks and downstream transfer tasks. For STS tasks, our evaluation takes the "all" setting and reports Spearman's correlation. 
You can evaluate any transformers-based pre-trained models using our evaluation code. For example,
```python
python evaluation.py --model_name_or_path `Replace with your model or path` --pooler cls_before_pooler --task_set sts --mode test
```
 
