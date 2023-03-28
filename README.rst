=======
CTMNeg
=======
**CTMNeg** is a neural topic model based on the VAE-based topic model CTM_. **CTMNeg** uses a negative sampling mechanism to improve the quality of the
generated topics.  In particular, during model training, we perturb the generated document-topic vector and use a triplet loss to encourage the document reconstructed from the correct document-topic vector to be similar to the input document and dissimilar to the document reconstructed from the perturbed vector.

.. _CTM: https://github.com/MilaNLProc/contextualized-topic-models

.. image:: https://github.com/AdhyaSuman/CTMNeg/blob/master/misc/Arch_Final.png
   :align: center
   :width: 2000px

Datasets
--------
Among the three datasets that we have used, **20NewsGroup (20NG)** and **M10** are available in OCTIS_. The another one dataset **GoogleNews (GN)** that we have used in the paper is added in the **preprocessed_datasets**.

Tutorials
---------
To optimize the hyperparameters of CTMNeg and to compare its performance with the existing topic models, we have used OCTIS_ which is an integrated framework for topic modeling.
Two notebooks are provided in the **examples** directory. First one is to run the hyperparameter optimization for CTMNeg, which also generates the experimental results with the optimized hyperparameters, and the second one is to run some existing topic models to compare the results.

.. |colab1| image:: https://colab.research.google.com/assets/colab-badge.svg
    :target: https://colab.research.google.com/github/AdhyaSuman/CTMNeg/blob/master/examples/HyperparameterOptimization_CTM_neg.ipynb
    :alt: Open In Colab

.. |colab2| image:: https://colab.research.google.com/assets/colab-badge.svg
    :target: https://colab.research.google.com/github/AdhyaSuman/CTMNeg/blob/master/examples/QuantitativeEvaluation.ipynb
    :alt: Open In Colab

 
+--------------------------------------------------------------------------------+------------------+
| Name                                                                           | Link             |
+================================================================================+==================+
| Hyperparameter optimization and result generation for CTMNeg                   | |colab1|         |
+--------------------------------------------------------------------------------+------------------+
| Getting results of some existing topic models for comparison                   | |colab2|         |
+--------------------------------------------------------------------------------+------------------+


.. _OCTIS: https://github.com/MIND-Lab/OCTIS

How to cite this work?
---------------------
This work has been accepted at ICON (International Conference on Natural Language Processing) 2022!

Read the paper:

1. `ACL Anthology`_

2. `arXiv`_

If you decide to use this resource, please cite:

.. _`ACL Anthology`: https://aclanthology.org/2022.icon-main.18/

.. _`arXiv`: https://arxiv.org/abs/2303.14951


::

    @inproceedings{adhya-etal-2022-improving,
    title = "Improving Contextualized Topic Models with Negative Sampling",
    author = "Adhya, Suman  and
      Lahiri, Avishek  and
      Kumar Sanyal, Debarshi  and
      Pratim Das, Partha",
    booktitle = "Proceedings of the 19th International Conference on Natural Language Processing (ICON)",
    month = dec,
    year = "2022",
    address = "New Delhi, India",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2022.icon-main.18",
    pages = "128--138",
    abstract = "Topic modeling has emerged as a dominant method for exploring large document collections. Recent approaches to topic modeling use large contextualized language models and variational autoencoders. In this paper, we propose a negative sampling mechanism for a contextualized topic model to improve the quality of the generated topics. In particular, during model training, we perturb the generated document-topic vector and use a triplet loss to encourage the document reconstructed from the correct document-topic vector to be similar to the input document and dissimilar to the document reconstructed from the perturbed vector. Experiments for different topic counts on three publicly available benchmark datasets show that in most cases, our approach leads to an increase in topic coherence over that of the baselines. Our model also achieves very high topic diversity.",
    }
  

Acknowledgment
--------------
All experiments are conducted using OCTIS_ which is an integrated framework for topic modeling.

**OCTIS**: Silvia Terragni, Elisabetta Fersini, Bruno Giovanni Galuzzi, Pietro Tropeano, and Antonio Candelieri. (2021). `OCTIS: Comparing and Optimizing Topic models is Simple!`. EACL. https://www.aclweb.org/anthology/2021.eacl-demos.31/

.. _OCTIS: https://github.com/MIND-Lab/OCTIS
