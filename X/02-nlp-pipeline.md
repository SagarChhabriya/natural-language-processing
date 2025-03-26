
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


- **Cleaning**
- HTML Tag Cleaning:
  - Use regex to remove tags
  - Emojis are not understandable by machine → Unicode Normalization `emoji_text.encode('utf-8')`
  - Spelling errors, gen-z typing, 

- **Basic Preprocessing**
  - Basic: Tokenization(Sentence, Word)
  - Optional: Stop Words Removal, Stemming, Lemmitization, Punctuation/digits Removal, Lowercasing, Language Detection
- **Advanced Preprocessing**
  - POS Tagging, Parsing, Coreference Resolution(Noun, Pronoun), etc.
 

### Feature Engineering
Feature Engineering in nlp pipeline is the process of converting the text to numeric so that our algorithms work on that data.

1. Feature Engineering in ML
   - In ML one has to manually engineer the features and that also requires domain knowldge
   - The result is interpretable   
2. Feature Engineering in DL
   - In DL the neural net will generate the features and one doesn't need to have the domain knowledge
   - Interpretability is lost

`NOTE`: The feature engineering depends on the problem you are solving there is no direct solution.


### Modelling
At this stage you've the right format data ready to be feeded to the algorithm.

- Stage 1: Modelling
  - Heuristic Approach
  - ML Algorithm
  - DL Algorithm
  - `Cloud APIs`

Selecting a modelling technique totally depends on the amount and quality of data you have and the nature of the problem that you are solving.
- Stage 2: Evaluation
  - Intrinsic Evaluation: Model Based/Technical Oriented: accuracy, precision, recall, confusion matrix
  - Extrinsic Evaluation: Business Oriented
