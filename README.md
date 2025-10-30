# Multi-Branch Speech Analysis for Parkinson’s Disease Detection
https://github.com/uanvson/Parkinson_MultiBranch

   ![Multi-Modal](https://raw.githubusercontent.com/uanvson/Parkinson_MultiBranch/refs/heads/main/Muli_modal_parkinson.png)

This study presents a multi-branch framework that integrates a pretrained CNN module with a pretrained Transformer module. By combining the CNN’s ability to extract local time–frequency representations with the Transformer’s capability to model global contextual dependencies, the proposed approach achieves superior performance in Parkinson’s disease detection

# Dataset
The Movement Disorders Voice Dataset used in this study was obtained from the publicly available Kaggle repos- itory (https://www.kaggle.com/datasets/cycoool29/movement- disorders-voice). It consists of a total of 180 voice recordings in .wav format, each sampled at a frequency of 16 kHz. Each recording has an average duration of approximately 1 minute and 15 seconds, splitted as:

Training set: 100 recordings
Test set: 40 recordings


# Method
MultiBranchPar.ipynb is main code to train the model for classification of PC and HC. We conduct 2 experiments
### 1. Base Pipeline CNN Only
In first experiment, we evaluate the performance of the baseline pipeline consisting only of the CNN module.

### 2. Proposed pipeline: CNN + Tranformer Fusion
In the second experiment, we test the pipeline that combines both the CNN and Transformer modules. The output features from the two branches are concated and fused using a gated self-attention mechanism before being passed to the final classification layer for DP and HC

# Conclusion
The fusion model that integrates both CNN and Transformer modules outperforms the CNN-only baseline in terms of accuracy and UAR. This improvement highlights the Transformer’s capability to model global dependencies within the speech features, leading to a more comprehensive representation and improved classification performance.
