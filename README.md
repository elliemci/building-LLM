# Building-LLM

The repository contains the jupyter notebooks for coding, pre-training and fine-tuning(coming soon) a Generative Pretrained Transformer, GPT-like LLM for text generation. The developing of a functional LLM model for the purpose of understanding the fundamental concepts and the transformer architecture, consists in the following stages:


1. Text data embedding
  1.1 Tokenization of text data code tokenizing_text.ipynb
  1.2 Token embedding code in token_embedding.ipynb  

2. Data preparation and sampling code in sliding_window_sampling.ipynb

3. Coding Attention Mechanism in attention_comp.ipynb

4. LLM top-down architecture code in gpt_implementation.ipynb

5. Pretraining on Unlabeled data - using a small raw text to predict the next word in a sentence with a self-supervised learning, where    the model generates its own labels from the input data
  5.1 Training and Validation - training.ipynb
  5.2 Decoding randomness control - randomness_control.ipynb
  5.3 Using OpenAI pretrained weights - openAIpretrained.ipynb
