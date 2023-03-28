# Delta-Modelling-ANN

## Introduction
This repository contains the scripts to train and test the models described in the two papers: "[Multi-Location Emulation of a Process-Based Salinity Model Using Machine Learning](https://www.mdpi.com/2073-4441/14/13/2030)" and "[Novel Salinity Modeling using Deep Learning for the Sacramento-San Joaquin Delta of California](https://www.mdpi.com/2073-4441/14/22/3628)".

Six different multi-variate neural networks, including MLP, ResNet, LSTM, GRU, Res-LSTM and Res-GRU, are implemented for salinity prediction at the Sacramento-San Joaquin Delta.

### Citation
If you use these models in your research, please cite:

    @article{qi2022multi,
    title={Multi-Location Emulation of a Process-Based Salinity Model Using Machine Learning},
    author={Qi, Siyu and He, Minxue and Bai, Zhaojun and Ding, Zhi and Sandhu, Prabhjot and Zhou, Yu and Namadi, Peyman and Tom, Bradley and Hoang, Raymond and Anderson, Jamie},
    journal={Water},
    volume={14},
    number={13},
    pages={2030},
    year={2022},
    publisher={MDPI}
    }

    @article{qi2022novel,
      title={Novel Salinity Modeling Using Deep Learning for the Sacramento--San Joaquin Delta of California},
      author={Qi, Siyu and He, Minxue and Bai, Zhaojun and Ding, Zhi and Sandhu, Prabhjot and Chung, Francis and Namadi, Peyman and Zhou, Yu and Hoang, Raymond and Tom, Bradley and others},
      journal={Water},
      volume={14},
      number={22},
      pages={3628},
      year={2022},
      publisher={MDPI}
    }



## What's in this repo
*  Code to train and test six different models on Google Colab or locally.
  - [Train_ANN_random_split.ipynb](colab_version/Train_ANN_random_split.ipynb): train a model on simulations or observed data, with random train-test splitting strategy.
  - [Train_ANN_on_Augmented_Dataset.ipynb](colab_version/Train_ANN_on_Augmented_Dataset.ipynb): train a model on multiple complete augmented simulations.
  - [Train_ANN_on_Observed_Data-Chronological-Test_on_Augmented_Data.ipynb](colab_version/Train_ANN_on_Observed_Data-Chronological-Test_on_Augmented_Data.ipynb): train a model on chronologically split observed data, and test on augmented datasets.
  - [Transfer_Learning_from_Augmented_to_Observed_Chronological.ipynb](colab_version/Transfer_Learning_from_Augmented_to_Observed_Chronological.ipynb): fine-tune a pre-trained model on chronologically split observed data. Note that the pre-trained model needs to be trained in advance before running this script.
*  Training and test data.
  - [Simulated_Dataset](data/Simulated_Dataset): DSM2 simulations.
  - [Augmented_Datasets](data/Augmented_Datasets): augmented datasets from simulations, where inputs are manually manipulated.
  - [Observed_Dataset](data/Observed_Dataset): real historical observations.
  - [martinez_stage1hr.csv](data/martinez_stage1hr.csv): hourly water stage at Martinez monitoring station, can be used as additional input feature.
