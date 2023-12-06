# AdaCSE
### Training
For each existing model to be improved, the samples that the model has difficulty recognizing are first selected as training data from `source data/chatgpt_pair.txt` or `source data/llama_pair.txt` and saved in  `. /data`.
### Training scripts
We provide training scripts `./run.sh`. Training scripts call `./train.py` for training.

### Evaluation
Our evaluation code for sentence embeddings is based on a modified version of [SentEval](https://github.com/facebookresearch/SentEval). It evaluates sentence embeddings on semantic textual similarity (STS) tasks and downstream transfer tasks. For STS tasks, our evaluation takes the "all" setting and reports Spearman's correlation. 
 
