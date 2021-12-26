# ShortRead
ShortRead is a Natural Language Processing based **text summarizer** which uses **extraction technique** to generate a concise and precise summary of voluminous texts while focusing on the sections that convey useful information, and without losing the overall meaning. 

Here we will be working to generate summary of the text present in ```edison.html``` file (which is downloaded/offline mode wikipedia page of following link:- https://en.wikipedia.org/wiki/Thomas_Edison).

Using word probability approach, reading time to read this (https://en.wikipedia.org/wiki/Thomas_Edison) article got reduced by 83.81%. While using tf-idf reading time got reduced by 77.50%.

Input

![bandicam 2021-12-26 20-48-47-239](https://user-images.githubusercontent.com/71775151/147412498-57fb4f19-675f-4f64-a92b-e0c22a6707fd.jpg)

Output

![bandicam 2021-12-26 20-49-07-008](https://user-images.githubusercontent.com/71775151/147412501-1c71aeee-3801-42a0-84de-3a51a9eb8c62.jpg)

## What makes ShortRead works?
Out of the two approaches to summarize texts in NLP: extraction and abstraction, ShortRead uses former one to generate the summary. The basic principle on which it works is that more important words a sentence will have, more the chances increase of that sentence to be part of the final summary. 

The frequency of words is calculated by using **frequency driven approaches** like: word probability and TF-IDF (Term Frequency Inverse Document Frequency). We have used both approaches to generate the summary.

The ```probability of a word``` w is determined as the number of occurrences of the word, f (w), divided by the number of all words in the input (which can be a single document or multiple documents). Words with highest probability are assumed to represent the topic of the document and are included in the summary. 

```TF-IDF```, a more sophisticated technique, assesses the importance of words and identifies very common words (that should be omitted from consideration) in the document(s) by giving low weights to words appearing in most documents. It is calculated by multiplication of ```term frequency``` and ```inverse document frequency``` (i.e. Term Frequency * Inverse Document Frequency). Term frequency (TF) is how often a word appears in a document, divided by how many words there are i.e. TF(t) = (Number of times term t appears in a document) / (Total number of terms in the document). Term frequency is how common a word is, inverse document frequency (IDF) is how unique or rare a word is i.e. IDF(t) = log_e(Total number of documents / Number of documents with term t in it).

Example,
Consider a document containing 100 words wherein the word apple appears 5 times. The term frequency (i.e., TF) for apple is then (5 / 100) = 0.05.
Now, assume we have 10 million documents and the word apple appears in one thousand of these. Then, the inverse document frequency (i.e., IDF) is calculated as log(10,000,000 / 1,000) = 4.
Thus, the TF-IDF weight is the product of these quantities: 0.05 * 4 = 0.20.

## Usage
Users can use ```summarizer.ipynb``` file (link: https://colab.research.google.com/drive/1ijYgJ032N-sy_ngoht88pZ7-wh9ybOxO?usp=sharing) to generate summary of the text of their own choice.

