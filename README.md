# bigram-language-model

Developing a Bigram Language Model 

The language model created interprets text from the book "Walden" by Henry David Thoreau. For anyone unfamiliar with how a bigram language model works, an explanation is provided below. Otherwise, feel free to skip to the workflow of the code analysis at the bottom.

~~~
A bigram language model is a statistical model used in natural language processing that predicts the probability of the next word in a sequence based on the previous word. In order to do that, the text is analyzed by breaking it down into pairs of adjacent words, referred to as "bigrams". Take the following text for a simple example: 

"According to the research, the 3 factors that seem to have the greatest influence on increasing our happiness are our ability to reframe our situation more positively, our ability to experience gratitude, and our choice to be kind and generous."

We'll start with the word "our", which appears 5 times in the text. The bigrams beginning with the word "our" are as follow: "our happiness", "our ability" (2x), "our situation", and "our choice". A bigram language model would then interpret the probability of the next word in the sequence to be: 

P("ability" | "our") = 2/5, or 0.4
P("happiness" | "our") = 1/5, or 0.2
P("situation" | "our") = 1/5, or 0.2
P("choice" | "our") = 1/5, or 0.2

The model is most likely to select "our ability", and then would continue moving forward, now analyzing the bigrams starting with "ability".
~~~

The workflow of the code analysis is:

1.  Download the text corpus to be interpreted at: https://www.gutenberg.org/files/205/205-0.txt
2.  Load this file into the working file directory of Python
3.  Run the file 'XXXXXXXXX', which will clean the original text (removing punctuation, and any text which is not part of the book), create a simple bigram language model, and return 100 sentences of text (with no more than 10 words in each sentence)
