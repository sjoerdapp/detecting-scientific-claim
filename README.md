# Claim Extraction for Scientific Publications

Detecting claim from scientific publication using discourse and sentence embedding.


## Training discourse model

Running AllenNLP to train discourse model as follows

```bash
python -m allennlp.run train pubmed_rct.json -s output --include-package discourse
```

or

```bash
allennlp train pubmed_rct.json -s output --include-package discourse
```

We point data location to Amazon S3 directly in `pubmed_rct.json`
so you do not need to download the data locally. Change `cuda_device` to `0` in  
`pubmed_rct.json` if you want to run on GPU.

**Note** that you have to remove `output` folder first before running.


## Predicting claim

We will release a dataset of scientific claims tagged by expert soon (in few months).


## Requirements

- [Pubmed RCT](https://github.com/Franck-Dernoncourt/pubmed-rct) - dataset
- [AllenNLP](https://github.com/allenai/allennlp)
- [spacy](https://github.com/explosion/spaCy)
