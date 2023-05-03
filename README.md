# NLP-Interview-Questions Basic
### What are the differences between TF-IDF and TF? some advantages of using TF-IDF over TF?
TF-IDF: Term Frequency-Inverse Document Frequency; <br>
TF: Term Frequency;

Difference:

TF-IDF is a numerical statistic that is intended to reflect how important a word is to the document in a collection of the corpus.
TF is a count of the number of times a word occurs in a document.

When TF is used, the frequency of the words appearing in the corpus will be used, which will be mostly populated with stop words such as "the", "a", "and", etc. So, most of the output will be skewed towards the stop words.
When TF-IDF is used, the numerical output is such that the output is not affected by the most common words in the corpus. The way that this is done is that the weights of the common words are diminished down, and the weights of the uncommon words are scaled up.

### What are the different types of text Preprocessing?
Steps of text preprocessing can be divided into 3 major types:

Tokenization: It is a process where a group of texts are divided into smaller pieces, or tokens. Paragraphs are tokenized into sentences, and sentences are tokenized into words.
Normalization: Database normalization is where the structure of the database is converted to a series of normal forms. What it achieves is the organization of the data to appear similar across all records and fields. Similarly, in the field of NLP, normalization can be the process of converting all the words to its lowercase. This makes all the sentences and tokens appear the same and does not complicate the machine learning algorithm.
Noise Removal: It is a process of cleaning up the text. Doing things such as removing characters which are not required, such as white spaces, numbers, special characters, etc.

Raw inputs --> Noise Removal(HTML tag, stop words, Punctuations, URL and white spaces) --> Text Normalization (Tokenization, Lemmatization, Stemming, Stentence Segmentation) --> Object Stadardisation (Regular Expression and Custom look up table) --> Cleaned Text


### What is a One-Hot Vector? How can they be used in Natural Language Processing? What are some disadvantages of using a One-Hot Vector for Natural Language Processing?

A one-hot is a group of bits which only has one high 1 bit and all other bits are low 0.
In Natural Language Processing, the one-hot vector can be used to represent a sentence in the form of a matrix of 1 x N size where N is the number of individual words in the corpus.
For example, the sentence "Peter picked a piece of pickled pepper" can be transformed into a matrix of 1 x 7 where each word is represented by the 7 columns. Hence the output of the sentence is: [0000001, 0000010, 0000100, 0001000, 0010000, 0100000, 1000000]

Dimensionality of the one-hot vector will increase as the size of the corpus increases. The vector is mostly populated with zeros with only one useful data.
Due to the dimensionality, an exponentially large memory will be used. For example, for a document of 50,000 vocabulary, we need 2,500,000,000 units of memory (50,000 * 50,000).
It is hard to extract meaning from the one-hot vectors. The output contains mostly zeros and a single one, so the vector can not create relationships between the different words.


###  What are some ambiguities faced in NLP?

Some ambiguities faced are:

<b>Lexical Ambiguity</b>: Words which have more than one meaning.<br>
<b>Syntactic Ambiguity</b>: Grammars used in sentences are ambiguous, and also more than one parsed tree is correct for a sentence given grammar.
<b>Semantic Ambiguity</b>: More than one semantic interpretation for a sentence.<br>
<b>Pragmatic Ambiguity</b>: It arises when the statement is not specific, and the context does not provide the information needed to clarify the statement.


### What is the use of PoS (Part of Speech) tagging?

PoS tagging is used to classify each word into its part of speech.<br>
Parts of speech can be used to find grammatical, or lexical patterns without specifying the word used. <br>
In English especially, the same word can be different parts of speech, so hence, PoS tagging can be helpful to differentiate between them.
