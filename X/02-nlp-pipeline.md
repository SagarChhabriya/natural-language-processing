
## End-to-End NLP Pipeline
NLP pipeline is a set of steps followed to build an end to end nlp software.

- Step 1: Data Acquisation: Gathering Data
- Step 2: Text Preprocessing
  - Step 2.1: Text Cleanup: Spelling mistakes, emojis
  - Step 2.2: Basic Preprocessing:
    - Tokenization, Stops words removal, punctuation removal
  - Step 2.3: Advanced Preprocessing: POS, Chunking, Conference Resolution   
- Step 3: Feature Engineering
  - Text to Numerical, Bag of Words, TF-IDF, Word2Vec
- Step 4: Modeling
- Step 5: Deployment: Deploy → Monitor → Update



### Data Acquisition
1. Internal Data: Already available 
  - Available in file
  - On Database (Talk to data eng team)
  - Less data → Data Augmentation
    - In this case we generate generate some fake data/synthetic data using existing data.
      - Ex: Bigram Flip, Back Translate, Additional Noise  
2. External Data
  - Public Dataset
  - Web Scraping: fetching customer reviews from daraz for developing a sentiment analyser of my newly created website.
  - API: Rapid API
  - PDF: pdf to text
  - Image: Image to text
  - Audio: Audio to text
3. Non-Existent
  - Heuristic Approach: Create manually

### Text Perparation
- Cleaning
- Basic Preprocessing
- Advanced Preprocessing


### Clearning
- HTML Tag Cleaning:
  - Use regex to remove tags
  - Emojis are not understandable by machine → Unicode Normalization `emoji_text.encode('utf-8')`

