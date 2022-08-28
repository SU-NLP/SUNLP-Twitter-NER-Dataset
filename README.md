# SUNLP-Twitter-NER-Dataset

This repository describes the Twitter dataset for Named Entity Recognition in Turkish. The dataset consists of 5,000 randomly selected tweets published between June 2020 and June 2021. 

## BERTurk and loodos's BERT model trained on our train set can be found in HuggingFace as [busecarik/berturk-sunlp-ner-turkish](https://huggingface.co/busecarik/berturk-sunlp-ner-turkish) and [busecarik/bert-loodos-sunlp-ner-turkish] (https://huggingface.co/busecarik/bert-loodos-sunlp-ner-turkish). 

## Dataset

Dataset is split into train/val/test sets with ratios of 70/15/15. Each line is separated with a tab character. The description of columns in each line is as follows:

| Column Name  | Description |
| ------------- | ------------- |
| tweet_id | Twitter ID of the tweet |
| start_pos | Position of starting character of an entity |
| end_pos | Position of last character of an entity |
| named_entity_type | Named Entity Type (Person, Location, Organization, Money, Time, Product, TV-Show) |


## Baseline Results

The baseline results obtained with different models in the validation and test sets are presented as follows: 

| Model                                                                                    | Validation F1 Score  | Test F1 Score
| ---------------------------------------------------------------------------------------- | -------------------- | -------------
| BiLSTM                                                                                   |                      | 
| BiLSTM-CRF                                                                               |                      | 
| [BERTurk (cased, 128k)](https://huggingface.co/dbmdz/bert-base-turkish-128k-cased)       | 84.65                | 83.64
| [BERT_loodos](https://huggingface.co/loodos/bert-base-turkish-cased)                     | 84.69                | 85.14
| [ConvBERTurk mC4 (cased)](https://huggingface.co/dbmdz/convbert-base-turkish-mc4-cased)  | 84.67                | 84.96

You can cite the following [paper](http://www.lrec-conf.org/proceedings/lrec2022/pdf/2022.lrec-1.484.pdf), if you use this dataset:

```bibtex
@InProceedings{ark-yeniterzi:2022:LREC,
  author    = {\c{C}ar\i k, Buse  and  Yeniterzi, Reyyan},
  title     = {A Twitter Corpus for Named Entity Recognition in Turkish},
  booktitle      = {Proceedings of the Language Resources and Evaluation Conference},
  month          = {June},
  year           = {2022},
  address        = {Marseille, France},
  publisher      = {European Language Resources Association},
  pages     = {4546--4551},
  url       = {https://aclanthology.org/2022.lrec-1.484}
}
```

For questions or comments regarding the data set, you can contact the author by e-mail:

Buse Çarık

busecarik@sabanciuniv.edu
