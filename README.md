# MRSCC - Sentence Completion Challenge #

The MRSCC (Microsoft Research Sentence Completion Challenge) is a task which involves the prediction of missing words in a sentence over five possible alternatives. The goal of this repo is to teach AI how to answer multiple choice questions. The two approaches considered were Ngrams and Neural language models (NLM). NLM are state-of-the-art models which were developed using transformer model architectures, examples are BERT developed by Google AI language [1] and BART created by Facebook [2]. On the other hand, N-grams are probabilistic models which can predict the next word in the sequence given the word present in the corpus. This approach uses Statistical concepts from NLP such as TF-IDF (term frequency-inverse distribution).

### Understanding the problem ###

![alt-text-1](/Project/img/the-simpsons-qa2.gif)

Five problems are considered: 

* Size of the dataset - In this coursework as the size of the MRSCC corpus data increases, bigrams and trigrams perform better than unigrams. This is due to the size of the training data increasing and fewer unknown words being present during the evaluation. However, these models were not able to reach scores above 30% given their limit to being unidirectional. While NLM such as BERT and ROBERTA make use of bi-directional word representation and achieve scores above 80%.

* N-grams - N-gram is a simple model that assigns probabilities to sequences of words and sentences and is one of the first language models or LM. The main drawback of using N-grams is the ability to account for unknown words. For instance, if the sentence contains the word ”rowers” (as seen in the next section), and that word was never seen during the calculation of the Ngram probability. The likely hood of having to return an error message or wrong answers is high. Nonetheless, some techniques that allow us to overcome this challenge are the addition of the ”UNK” token for each word or a given new sequence, Laplacian smoothing, discounting and lowering the context window. Lastly, the time it requires to access the probability dictionary for each word in the data can be exhaustive to the CPU thus requiring a long training time.

* NLM - Neural language models come from Neural networks, a concept from machine learning. In neural networks, the representation of words is changed to vectors or word embedding. That allows the computer to encode the words in the sentences and learn each representation as a vector space. The best accuracy was the off-the-shelf Roberta-Large with 86% closer to the human judgement score of 90%. Nonetheless, the size of Roberta large is greater compared to the other models since more corpus training data was used during training.

* Fine-tuning -  The advantage of NLM is the ability to fine-tune using custom data. When trained with 15 books from Colyn Doyle where most of the questions are derived, the accuracy of BERT models increased by one percentage point. The percentage increase was given the time it takes to fine-tune this particular model (6 epochs). In some instances, fine-tuning decreased the accuracy of the off-the-shelf models such as Roberta by two percentage points. This is given this particular model has over 24 transformers blocks and 1024 hidden layers which are affected by bias when trying to fine-tune this version of the model given the training data used during train containing unfiltered corpus from the internet [3].

* Measuring Performance - perplexity as a measure of performance is not a good metric since the goal of the AI is to select the correct answer. Nonetheless, perplexity allows us to measure how well the model understands the data. The models that had lower accuracy in this case NLM (Roberta- Large) with values below a score of 3. During this research lower perplexity equated to a model having higher accuracy. On the other hand models with higher perplexity values such as unigram as seen in Figure 5 did not perform well.

### Results and Visualization ###

![alt-text-1](/Project/img/res1.png)

![alt-text-1](/Project/img/res2.png)

![alt-text-1](/Project/img/sent1.png)

![alt-text-1](/Project/img/sent2.png)

### Repo structure ###

This project was done using python (jupyter-notebook), and in the Project folder there are 3 other subsequent folders namely:

* src - or source code where the different implementations of the N-gram and BERT are located. 
* pdf - where summary of the work is present. 
* img - has the visualization gif used in the repo 😁.

To run the implementations located in src simply select the '.ipynb' file. 

*Note:* The complete report for this project will be made avaliable for the time being.

### References ###

1. NLP lecturer and TA's @ Sussex uni

2. Github and google

3. Devlin, J., Chang, M.-W., Lee, K., Google, K. and Language, A. (2019). BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding. [online] Available at: https://arxiv.org/pdf/1810.04805.pdf.

4. Lewis, M., Liu, Y., Goyal, N., Ghazvininejad, M., Mohamed, A., Levy, O., Stoyanov, V., Zettlemoyer, L. and Ai, F. (2019). BART: Denoising Sequence-to-Sequence Pre-training for Natural Language Generation, Translation, and Comprehension. [online] Available at: https://arxiv.org/pdf/1910.13461.pdf.

5. Ferm, J. (n.d.). Methods for sentence completion. [online] Available at: https://fileadmin.cs.lth.se/cs/education/EDAN60/Reports/2013/jonatan.pdf.

6. Zweig, G. and Burges, C.J.C. (2011). The microsoft research sentence completion challenge. [online] Available at: https://www.microsoft.com/en-us/research/publication/the-microsoftresearch-sentence-completion-challenge/

7. Daniel, J. and Martin, J. (2021). Speech and Language Processing. [online] Available at: https://web.stanford.edu/jurafsky/slp3/3.pdf.


### Who do I talk to? ###

* Repo owner Neil Fabião -> @neilfabiao ✌🏾

![](https://komarev.com/ghpvc/?username=neilNLP120&color=blue)
