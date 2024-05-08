# Building-LLM

The repository contains the jupyter notebooks for coding, pre-training and fine-tuning(coming soon) a Generative Pretrained Transformer, GPT-like LLM for text generation. The development of a functional LLM model is done with code examples of the fundamental components and GPT model architecture implemented as classes in the following stages:


1. Text data embedding <br>
&nbsp; 1.1 Word tokenization of text data which includes splitting text into words, removing whitespaces and special characters  with regular expressions, converting words into tokens, building vocabulry and mapping tokens to IDs, extending vocabulary to tokenize unknown words and Byte Pair Encoding with [tiktoken library](https://github.com/openai/tiktoken) code in [tokenizing_text.ipynb](https://github.com/elliemci/building-LLM/blob/main/tokenizing_text.ipynb) <br>
&nbsp; 1.2 Input-targeet pairs and token embedding - code in [token_embedding.ipynb](https://github.com/elliemci/building-LLM/blob/main/token_embedding.ipynb) implements a data loader of input-target pairs for next-word prediction with a sliding window over the training dataset and eexample of Embedding layer with token and positional encoding. <br>

4. Implementation of a causal self-attention modulee with attention mask and stacking multiple causal atteention modules into a multi-head atteention in [attention_comp.ipynb](https://github.com/elliemci/building-LLM/blob/main/attention_comp.ipynb) <br>

5. LLM top-down architecture of GPT-like model class consisting  of token and positional embeddings, drop out, a series of transformer blocks, a final normalization layer and a linear output layer. Gaussian Error Linear Unit activation class and Feed forwarrd class with forward method that describes the data flow through the model, with added skip conections that create a shorter path for the gradient to flow through the network by skippinng one or more layers and doing so resolve the vanisshing gradient problem in [gpt_implementation.ipynb](https://github.com/elliemci/building-LLM/blob/main/gpt_implementation.ipynb) <br>

6.Pretraining on Unlabeled data involves evaluation of the model generated text, calculating the training and validation set losses.
&nbsp; 6.1 Training loop using cross entropy and AdamW optimizer which prrevent oveerfitting by penalizing large weights, and Validation implemented in [training.ipynb](https://github.com/elliemci/building-LLM/blob/main/training.ipynb) <br>
&nbsp; 6.2 Randomness control with temperature scaling and top-k sampling code examples in [randomness_control](https://github.com/elliemci/building-LLM/blob/main/randomness_control.ipynb) <br>
&nbsp; 6.3 Using public OpenAI pretrained weights [openAIpretrained.ipynb](https://github.com/elliemci/building-LLM/blob/main/opeenAIpretrained.ipynb) <br>
