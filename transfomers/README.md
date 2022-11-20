# PYTORCH-TRANSFORMERS
- https://pytorch.org/hub/huggingface_pytorch-transformers/


# Bert vs transformer
- https://ai.stackexchange.com/questions/23221/how-is-bert-different-from-the-original-transformer-architecture#:~:text=BERT%20is%20only%20an%20encoder,is%20a%20transformer%2Dbased%20model.
```
What is BERT?
BERT stands for Bidirectional Encoder Representations from Transformers, so, as the name suggests, it is a way of learning representations of a language that uses a transformer, specifically, the encoder part of the transformer.

What is the difference between the transformer and BERT?
BERT is a language model, i.e. it represents the statistical relationships of the words in a language, i.e. which words are more likely to come after another word and stuff like that. Hence the part Representations in its name, Bidirectional Encoder Representations from Transformers.

BERT can be trained in an unsupervised way for representation learning, and then we can fine-tune BERT on the so-called downstream tasks in a supervised fashion (i.e. transfer learning). There are pre-trained versions of BERT that can be already fine-tuned (e.g. this one) and used to solve your specific supervised learning task. You can play with this TensorFlow tutorial to use a pre-trained BERT model.

On the other hand, the original transformed was not originally conceived to be a language model, but to solve sequence transduction tasks (i.e. converting one sequence to another, such as machine translation) without recurrent connections (or convolutions) but only attention.

BERT is only an encoder, while the original transformer is composed of an encoder and decoder. Given that BERT uses an encoder that is very similar to the original encoder of the transformer, we can say that BERT is a transformer-based model. So, BERT does not use recurrent connections, but only attention and feed-forward layers. There are other transformed-based neural networks that use only the decoder part of the transformer, for example, the GPT model.

BERT uses different hyper-parameters than the ones used in Attention is all you need to achieve the best performance. For example, it uses 12 and 16 "attention heads" (please, read the transformer paper to know more about these "attention heads") rather than 8 (although in the original transformer paper the authors experimented with a different number of heads).

BERT also uses segment embeddings, while the original transformer only uses word embeddings and positional encodings.

There are probably other small differences that I missed, but, after having read the paper Attention is all you need and quickly read some parts of the BERT paper, these seem to be the main differences.

When to use BERT and the transformer?
Although I never used them, I would say that you want to use BERT whenever you want to solve an NLP task in a supervised fashion, but your labeled training dataset is not big enough to achieve good performance. In that case, you start with a pre-trained BERT model, then fine-tune it with your small labeled dataset. You probably need to add specific layers to BERT to solve your task.



```