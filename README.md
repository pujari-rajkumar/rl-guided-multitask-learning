This repo contains the annotated dataset and code to replicate experiments and ablation studies from ACL 2022 long paper <a href="https://rajkumar-pujari.com/reinforcement_guided.html">Reinforcement Learning Guided Multi-Task Learning for Stereotype Detection</a> by Rajkumar Pujari, Erik Oveson, Priyanka Kulkarni and Elnaz Nouri.

<h3>Dataset</h3>
Fine-grained steretype detection dataset that was decribed in the paper is in the annotated_data.csv file. Each data point was annotated by three MTurk annotaters with two labels: 1) whether the text contains explicit and intentional stereotype and 2) whether the text contains implicit stereotypical association. Majority vote from the three annotaters was assigned as the data label.

<h3>Code</h3>

The <tt>notebooks/</tt> folder contains the following jupyter notebooks:

1) <tt> bart_large-gpu1-policy_network_training.ipynb </tt>
  
2) <tt> bert_base-gpu0-policy_network_training.ipynb </tt>
  
3) <tt> bert_large-gpu0_1-policy_network_training.ipynb </tt>
  
4) <tt> xlnet_large-gpu1_1-policy_network_training.ipynb </tt>
  
5) <tt> rl_multitask_data_utils.ipynb </tt>
  
6) <tt> ablation1-bert_base-gpu0.ipynb </tt>
  
7) <tt> ablation2-bert-base-gpu0.ipynb </tt>

Data utils notbook contains code to run the pre-processing raw datasets into processes format. You would need to change the name of the PLM tokenizer and model to generate embeddings for different PLMs. If you don't want to pre-process the data yourself, you may download the processed data files from <a href="https://drive.google.com/drive/folders/1_PKGwIrGdCfGeNfQqAckwJvyzrc9KfiV?usp=sharing">here</a>.

The policy training notebooks contain code for training all the experiments using the .pkl files provided <a href="https://drive.google.com/drive/folders/1_PKGwIrGdCfGeNfQqAckwJvyzrc9KfiV?usp=sharing">here</a>.

The ablations study notebooks contain code to replicate the MLT prior impact and neightbor task impact ablation studies as described in the paper.



