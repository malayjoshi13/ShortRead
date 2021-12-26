# ShortRead
ShortRead is a Natural Language Processing based **text summarizer** which uses **extraction technique** to generate a concise and precise summary of voluminous texts while focusing on the sections that convey useful information, and without losing the overall meaning. 

Here we will be working to generate summary of the text present in ```edison.html``` file (which is downloaded/offline mode wikipedia page of following link:- https://en.wikipedia.org/wiki/Thomas_Edison).

Input

![bandicam 2021-12-26 20-48-47-239](https://user-images.githubusercontent.com/71775151/147412498-57fb4f19-675f-4f64-a92b-e0c22a6707fd.jpg)

Output

![bandicam 2021-12-26 20-49-07-008](https://user-images.githubusercontent.com/71775151/147412501-1c71aeee-3801-42a0-84de-3a51a9eb8c62.jpg)

## What makes ShortRead works?
Out of the two approaches to summarize texts in NLP: extraction and abstraction, ShortRead uses former one to generate the summary. The basic principle on which it works is that more important words a sentence will have, more the chances increase of that sentence to be part of the final summary. 

The frequency of words is calculated by using **frequency driven approaches** like: word probability and TF-IDF (Term Frequency Inverse Document Frequency). We have used both approaches to generate the summary.

## Usage
Users can use ```summarizer.ipynb``` file (link: https://colab.research.google.com/drive/1ijYgJ032N-sy_ngoht88pZ7-wh9ybOxO?usp=sharing) to generate summary of the text of their own choice.

