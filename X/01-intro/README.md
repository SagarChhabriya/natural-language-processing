## NLP
  - Subfield of linguistics, CS, and AI.
  - How to program computer to process and analyze large aomunts of natural language data.

### Real World Applications
  - Contextual Advertisements
  - Email Filtering
  - Social Media
    - removing adult content, opinion mining
  - Search Engines
    - one line definition instead of just showing the websites 
  - Chatbots


### Commong NLP Tasks
1. Text/Document Classification
2. Sentiment Analysis
3. Information Retrievel (NER)
4. Parts of Speech (POS Tagging)
5. Language Detection and Machine Translation
6. Conversational Agents
7. Knowledge Graph
8. Text Summarization
9. Topic Modeling (Context related info -- fetch legal info from a doc)
10. Next Word Predictor/Grammar Checking
11. Texting Parsing, Speech to Text



### Approaches to NLP
1. Heuristic Methods (Jugaadi)
  - Rule Based Approach
  - Ex: Regex, Wordnet(lexical dictionary), open mind common sense
  - Less Error, Still Used
2. Machine Learning Based Methods
  - Human fails at defining rules for large amount data so there comes the ML.
  - Algorithms: Logistic Regression, SVM, LDA for Topic Modeling, Hidden Markov Methods(HMM) for POS
3. Deep Learning Based Methods
  - In ML we need to convert the text into numeric and we loose the sequential info of the data. In ML features engineering is done manually but DL does itself.
  - Ex: This is my house → Sequential, House this is mine → Non-Sequential
  - Algorithms:
    - RNN (Recurrent Neural Networks): Used in earlier days and it is not able to remember the context of very long text/paragraph. Solution: LSTM
    - LSTM (Long Short Term Memory): Can remember the context of very long text.
    - CNN (Convolutional Neural Networks): Mostly used for image classification, but it can also be used for text classification.
    - Transformers (2015): Provides attention on part of text e.g., BERT.
    - Autoencoder




### Challenges in NLP
1. Ambiguity
  - Ex: Chalo pooja karte hain.
2. Contextual Words
  - I `ran` to the store becuase we `ran` out of the milk.
3. Colloquialism and Slang
  - Piece of cake, pulling your leg, break a leg
4. Synonyms
5. Irony, Sarcasm & Tonal difference
  - That's just what I needed today.
6. Spelling Erros
7. Creativity: Poems, Dialogue, Scripts
8. Diversity: A lot of languages

