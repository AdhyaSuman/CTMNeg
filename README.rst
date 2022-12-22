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

Citation
--------
If you find this useful you can cite the following paper :

::

Suman Adhya, Avishek Lahiri, Debarshi Kumar Sanyal, and Partha Pratim Das. 2022. Improving Contextualized Topic Models with Negative Sampling. In Proceedings of the 19th International Conference on Natural Language Processing (ICON), Indraprastha Institute of Information Technology, Delhi, India. NLP Association of India (NLPAI).
