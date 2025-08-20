# Blogs

- [GFG Blog](https://www.geeksforgeeks.org/advanced-natural-language-processing-interview-question/)




# General Qs
1. Describe how you would implement a chatbot using NLP?
2. Language Modeling vs Topics Modeling 
    - LM: (Supervised | GPT | Unigram, bigram, n-gram, NLM(RNNs, LSTM, Transformers))
    - TM: (Unsupervised | LDA, LSA) Dim reduction techs: LSA, LDA. Use case: Document clustering, content recommendation
















# General Answers

- NLP Pipeline

| Step                        | What Happens              | Tools / Examples              |
| --------------------------- | ------------------------- | ----------------------------- |
| **1. Data Collection**      | Gather text data          | Tweets, reviews, articles     |
| **2. Preprocessing**        | Clean and tokenize text   | NLTK, spaCy, regex            |
| **3. Representation**       | Convert to vectors        | TF-IDF, Word2Vec, BERT        |
| **4. Training**             | Learn patterns from data  | sklearn, PyTorch, TensorFlow  |
| **5. Testing**              | Evaluate on new data      | Accuracy, F1, etc.            |
| **6. Prediction**           | Use on real-world input   | Chatbots, search engines      |
| **7. Tuning / Fine-tuning** | Improve model performance | Grid search, BERT fine-tuning |


- Tokenization: process of converting text into smaller units called tokens, which can be words, subwords, or characters.
- Stemming: Rule Based
- Lemmetization: Morphological analysis


- Language Modeling: Predicts the next word or token in a sequence.
- Topic Modeling: Identifies latent topics in a collection of documents.
- Text Classification: Assigns categories or labels to texts.
- Named Entity Recognition: Identifies entities like people, places, and dates.
- Text Summarization: Condenses a large text into a shorter version.
- Question Answering: Answers questions based on a text or knowledge base.
- Text Generation: Produces new text based on a prompt.
- Machine Translation: Translates text from one language to another.
- Coreference Resolution: Resolves references to the same entity in a text.

- GPT: Unidirectional decoder for text generation(next word prediction).
- BERT: Bidirectional encoder for text understanding (questions answering).
- sequence-to-sequence models(Encoder & Decoder): designed to transform one sequence into another, commonly used in tasks like translation or summarization.







- self supervised learning: unlabeled data to train a model by generating its own labels or using information within the data itself for supervision. Ex: Filling in the blanks.
- Evalution metrics used for NLP models 
    - Accuracy, Precision, Recall, F1-Score, BLEU Score

- Choosing Embedding Model: Use TF-IDF for lightweight keyword tasks on small datasets; Word2Vec for scalable similarity; BERT embeddings for deep, context-sensitive

understanding.
- Contrastive Learning: Bring similar things closer, push different things apart.
    - Loss Functions: Simple distance difference, Triplet loss 
    - What can be contrasted?: Orginal vs paraphrased sentence
- How do you handle OOV: 
    - Subword Models like BERT, GPT
    - Character level Models: Some models work one letter at a time, so OOV isn’t a problem at all.
- embedding: converting a word/sentence/paragraph i.e., text into a vector(a list of numbers that captures its meaning and relationship).
    - Types:
        - word embeddings: one word, cat
        - sentence embeddings: whole sentence, I love coding
        - document embeddings: paragraph/doc, This is a file with list of NLP questions .... → long vector
    - Methods:
        - word2vec: context based, king-man+woman=queen
        - glove:Uses global word co-occurrence counts
        - FastText: Breaks words into subwords, helps with OOV words
        - BERT / GPT Embeddings: Contextual: the word "bank" has a different vector in "river bank" vs. "money bank"





- Keyword Normalization: preprocessing steps like lowercasing, stemming, lemmatization, etc. To make tokens uniform, reduce sparsity. It helps with data cleaning, but not directly dimensionality reduction in the mathematical sense.

- Latent Semantic Indexing: Statistical Model(distributions, relations b/w variables, counting frequency, frequency distributions)

- Latent Dirichlet Allocation: Probablistic Model(treat everything as random variables, probability distributions)

