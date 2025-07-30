Impact-Model Demo 
========================================================

ENVIRONMENT
-----------
Python 3.10

Required pip/conda packages:
    pandas          >= 1.5
    numpy           >= 1.23
    scikit-learn    >= 1.2      # for k-means splitter
    matplotlib      >= 3.7
    jupyterlab OR notebook

Quick install (conda):
    conda create -n impact-demo python=3.10 pandas numpy scikit-learn matplotlib jupyterlab
    conda activate impact-demo


DATA SOURCE
-----------
File used:  Train_Dst_NoAuction_DecPre_CF_1.txt
Dataset:    FI-2010 Limit Order Book, public mirror on Kaggle / Zenodo.
The “DecPre” variant contains 40 limit-order-book features per snapshot
but no stock_id.  (Other data sets were hard to come by. I tried Coinbase, but the data was pretty bad.)

Instead, I clustered first-level ask price into 5 groups and keep
one pseudo-ticker for the demo.

RUNTIME
-------
Open `impact_model_demo.ipynb` in JupyterLab and run all cells.
Full pipeline (Parts A-F) completes in ~3 minutes on a laptop.

Outputs:
    impact_stock_<label>.pdf   –  g(x) curve + linear β fit
    alloc_stock_<label>.pdf    –  optimal execution schedule
Saved to the working directory.


LICENSE
-------
Notebook code MIT, data per FI-2010 license (free academic use).
