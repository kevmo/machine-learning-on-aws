**TF-IDF** stands for **Term Frequency-Inverse Document Frequency**. It's a numerical statistic that reflects how important a word is to a document in a collection or corpus. The idea behind it is to weight terms based on how frequent they are in a document, but also to discount those terms that are frequent across many documents. It's particularly useful in text mining and information retrieval (like in search engines).

Let's break down the TF-IDF:

1. **Term Frequency (TF)**: This measures the frequency of a term in a document.
   \[ \text{TF}(t) = \frac{\text{Number of times term t appears in a document}}{\text{Total number of terms in the document}} \]
2. **Inverse Document Frequency (IDF)**: This measures how unique or rare a term is across the entire corpus.
   \[ \text{IDF}(t) = \log_e\left(\frac{\text{Total number of documents}}{\text{Number of documents with term t in it}}\right) \]

The overall **TF-IDF** score of a term in a document is the product of its TF and IDF scores:
\[ \text{TF-IDF}(t) = \text{TF}(t) \times \text{IDF}(t) \]

#### Example:

Imagine we have a collection of three documents:

1. "I love machine learning"
2. "I love deep learning"
3. "Deep blue beats Kasparov at chess"

Let's compute the TF-IDF for the term "love":

**TF**:

- In the first document: TF("love") = 1/4 = 0.25 (because "love" appears once out of 4 words)
- In the second document: TF("love") = 1/4 = 0.25
- In the third document: TF("love") = 0 (because "love" doesn't appear in this document)

**IDF** (across all documents):
\[ \text{IDF}("love") = \log_e\left(\frac{3}{2}\right) \]
(where 3 is the total number of documents, and 2 is the number of documents containing the term "love").

Now, the TF-IDF score for "love" in the first document is:
\[ \text{TF-IDF}("love") = 0.25 \times \log_e\left(\frac{3}{2}\right) \]
(And similarly, you'd compute for the second document)

The term "love" will get a relatively lower TF-IDF score in a document from a large corpus where the term "love" is frequently mentioned, but a high score in documents where it's rare but does appear.

In practice, TF-IDF is commonly used with tools like Scikit-learn in Python, which provides built-in functions to compute TF-IDF scores for any given corpus.
