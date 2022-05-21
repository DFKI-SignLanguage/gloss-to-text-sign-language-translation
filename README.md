# Neural Machine Translation Methods for Sign Language Translation

This repository provides complementary material to aid the replication of the experiments described in the paper [Using Neural Machine Translation Methods for Sign Language Translation](https://aclanthology.org/2022.acl-srw.21) (Angelova et al., ACL 2022). 


## Introduction

In this paper, we examine methods and techniques, proven to be helpful for the text-to-text translation of spoken languages in the context of gloss-to-text translation systems, where the glosses are the written representation of the signs. We present one of the first works that include experiments on both parallel corpora of the German Sign Language (PHOENIX14T and the Public DGS Corpus). We experiment with two NMT architectures with optimization of their hyperparameters, several tokenization methods and two data augmentation techniques (back-translation and paraphrasing). 

Through our investigation we achieve a substantial improvement of 5.0 and 2.2 BLEU scores for the models trained on the two corpora respectively. 
Our RNN models outperform our Transformer models, and the segmentation method we achieve best results with is BPE, whereas back-translation and paraphrasing lead to minor but not significant improvements. 

## Content 

The structure of the repository is as following:

 * `notebooks`: Python notebooks containing the code for reproducing the experiments, 
   *  splitting training and test set for the DGS corpus
   *  measuring statistics for the DGS corpus
   *  extract glosses and german intepretation from the DGS corpus
   *  custom tokenization of the DGS corpus
   *  measure overlap between training, dev and test splits of the DGS corpus
 * `training scripts`: bash files including SLURM commands to execute Marian-NMT for training the NMT models reported in the paper
 * `data`: the plain-text versions of the paraller corpora for both the DGS and the Phoenix corpora. It includes the training, dev and test split for both the Phoenix and DGS corpus. Additionally, one can find tokenized, stemmed and augmented versions as reported in the paper.  

## Citation

This work has been done with the aim to contribute to the research towards the automatic translation of sign languages. We encourage any further research on top of our work and we are happy to answer related questions. The code is released under the GPL-3.0 License.

If you use the code or derivatives of this repository, please cite:

```
@inproceedings{angelova-etal-2022-using,
    title = "Using Neural Machine Translation Methods for Sign Language Translation",
    author = {Angelova, Galina  and
      Avramidis, Eleftherios  and
      M{\"o}ller, Sebastian},
    booktitle = "Proceedings of the 60th Annual Meeting of the Association for Computational Linguistics: Student Research Workshop",
    month = may,
    year = "2022",
    address = "Dublin, Ireland",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2022.acl-srw.21",
    pages = "273--284",
}
```

More citation formats [here](https://aclanthology.org/2022.acl-srw.21/)

Please note that the corpora ([Phoenix 2014T](https://www-i6.informatik.rwth-aachen.de/~koller/RWTH-PHOENIX-2014-T/) and [DGS Corpus](https://www.sign-lang.uni-hamburg.de/meinedgs/ling/start_en.html)) have their own licenses and any use of them should be conforming with them and include the appropriate citations. 

