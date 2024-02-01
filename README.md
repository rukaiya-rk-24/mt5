# mt5
Optimizing mT5 for a single language involves pruning redundant embeddings, significantly reducing the model’s size without losing quality. The idea is similar to one in the paper Load What You Need: Smaller Versions of Multilingual BERT. We use the original tokenizer to process corpus of one language, count the frequencies of different tokens, and preserve only the tokens that were used frequently enough, pruning all the others.

The method involves selecting a subset of the vocabulary (including a mix of the targeted language and some English tokens for bilingual capacity), updating the model’s input and output embeddings accordingly, and adjusting the tokenizer. This results in a streamlined model, more efficient for specific language tasks, and considerably smaller in size. For a complete guide and the practical implementation of this optimization, in my attached code file here I have extracted tokens for only Punjabi language.

