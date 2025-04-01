### **Text Representation Techniques: From Basic to Advanced**

---

### **1. One-Hot Encoding (OHE)**
**Representation**: Binary (0/1) presence of words  
**Key Features**:
- Simplest form of text representation
- Creates extremely sparse vectors
- No semantic or frequency information

**Code Example**:
```python
from sklearn.feature_extraction.text import CountVectorizer
docs = ["people watch techhub", "techhub watch techhub"]
vectorizer = CountVectorizer(binary=True)
ohe_matrix = vectorizer.fit_transform(docs)
print(ohe_matrix.toarray())
```

**Real-World Use**: Spam detection using keyword presence

---

### **2. Bag of Words (BoW)**
**Representation**: Word frequency counts  
**Improvements Over OHE**:
- Captures word frequency
- Still sparse but less than OHE

**Code Example**:
```python
vectorizer = CountVectorizer()  # Default counts frequencies
bow_matrix = vectorizer.fit_transform(docs)
print(bow_matrix.toarray())
```

**Real-World Use**: News article categorization

---

### **3. TF-IDF**
**Representation**: Weighted word frequencies  
**Improvements Over BoW**:
- Downweights common words
- Highlights important terms

**Code Example**:
```python
from sklearn.feature_extraction.text import TfidfVectorizer
vectorizer = TfidfVectorizer()
tfidf_matrix = vectorizer.fit_transform(docs)
print(tfidf_matrix.toarray())
```

**Real-World Use**: Search engine ranking

---

### **4. Bag of N-Grams**
**Representation**: N-gram frequency counts  
**Improvements Over TF-IDF**:
- Captures local word order
- Preserves phrases

**Code Example**:
```python
vectorizer = CountVectorizer(ngram_range=(1,2))  # Unigrams+bigrams
ngram_matrix = vectorizer.fit_transform(docs)
print(ngram_matrix.toarray())
```

**Real-World Use**: Sentiment analysis (capturing negations)

---

### **5. Word2Vec**
**Representation**: Dense word embeddings (50-300D)  
**Improvements Over N-Grams**:
- Captures semantic relationships
- Fixed-length vectors

**Code Example**:
```python
from gensim.models import Word2Vec
sentences = [d.split() for d in docs]
model = Word2Vec(sentences, vector_size=50)
print(model.wv["techhub"])  # Word vector
```

**Real-World Use**: Product recommendations

---

### **6. Doc2Vec**
**Representation**: Document embeddings  
**Improvements Over Word2Vec**:
- Whole document representation
- Better for short texts

**Code Example**:
```python
from gensim.models import Doc2Vec
from gensim.models.doc2vec import TaggedDocument
documents = [TaggedDocument(d.split(), [i]) for i,d in enumerate(docs)]
model = Doc2Vec(documents, vector_size=50)
print(model.dv[0])  # Document vector
```

**Real-World Use**: Legal document similarity

---

### **7. BERT**
**Representation**: Contextual embeddings  
**Improvements Over Doc2Vec**:
- Understands word context
- State-of-the-art performance

**Code Example**:
```python
from transformers import BertTokenizer, BertModel
tokenizer = BertTokenizer.from_pretrained('bert-base-uncased')
model = BertModel.from_pretrained('bert-base-uncased')
inputs = tokenizer("people watch techhub", return_tensors="pt")
outputs = model(**inputs)
print(outputs.last_hidden_state.shape)  # Contextual embeddings
```

**Real-World Use**: Advanced chatbots and translation

---

### **Comparison Summary**

| Technique | Preserves Order | Semantics | OOV Handling | Dimensionality | Best For |
|-----------|-----------------|-----------|--------------|----------------|----------|
| OHE | ❌ | ❌ | ❌ | High | Baseline models |
| BoW | ❌ | ❌ | ❌ | High | Frequency analysis |
| TF-IDF | ❌ | ❌ | ❌ | High | Search engines |
| N-Grams | ✅ Local | ❌ | ❌ | Very High | Short phrases |
| Word2Vec | ❌ | ✅ | ✅ Partial | Low | Word analogies |
| Doc2Vec | ❌ | ✅ Partial | ✅ Partial | Low | Doc similarity |
| BERT | ✅ Full | ✅ | ✅ Best | Very High | Complex NLP |

---

### **Evolutionary Insights**
1. **From Sparsity to Density**: OHE → BoW → TF-IDF (reducing sparsity) → Word2Vec (dense vectors)
2. **From Frequency to Meaning**: Count-based → Distributed representations
3. **From Local to Global Context**: N-grams (local) → BERT (global)
4. **From Words to Documents**: Word2Vec (words) → Doc2Vec/BERT (documents)

---

### **Practical Guidance**
- **Start Simple**: Use TF-IDF for baseline models
- **Balance Complexity**: Word2Vec offers good semantics with moderate compute
- **State-of-the-Art**: BERT when resources allow and context matters
- **Special Cases**:
  - N-grams for sentiment/negation
  - Doc2Vec for document similarity
  - OHE/BoW for interpretable models

