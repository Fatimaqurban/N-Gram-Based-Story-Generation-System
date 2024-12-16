---

# **N-Gram Based Urdu Story Generation System**

This project implements an **N-gram language model** to generate sentences and paragraphs from an Urdu story corpus. The system is capable of generating text using **Unigram, Bigram, and Trigram models**, showcasing the probabilistic relationships between words.

## **Features**
1. **Corpus Preprocessing**  
   - Tokenizes Urdu story data using **NLTK**'s `word_tokenize`.  
   - Extracts word frequencies for Unigram, Bigram, and Trigram models.  

2. **N-Gram Models**  
   - **Unigram Model**: Generates sentences by selecting words randomly based on frequency.  
   - **Bigram Model**: Predicts the next word based on the previous word's frequency.  
   - **Trigram Model**: Predicts the next word based on the previous two words.  

3. **Story Generation**  
   - Generates random sentences with lengths between **5 to 19 words**.  
   - Combines sentences into structured **paragraphs** (default: 3 paragraphs with 5 sentences each).  

4. **Statistical Insights**  
   - Displays **top starting words**, unigram frequencies, bigram pairs, and trigram sequences for verification.  

## **Project Structure**
- **Tokenization**: Tokenizes sentences and constructs N-gram frequency distributions.  
- **Model Training**: Builds Unigram, Bigram, and Trigram models from the corpus.  
- **Text Generation**:  
   - Randomized starting word selection.  
   - Next word prediction using probabilistic sampling based on N-gram models.  

## **Requirements**
- **Python 3.x**  
- **NLTK** (Natural Language Toolkit)  
- **Pandas**  

Install required libraries using:  
```bash
!pip install nltk pandas
```

## **Setup Instructions**
1. Mount your Google Drive in Google Colab:  
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```
2. Load the Urdu story corpus:  
   Ensure your CSV file (`urdu_stories.csv`) is stored at the specified path:  
   ```python
   df = pd.read_csv('/content/drive/My Drive/NLP/Assignment 4/urdu_stories.csv', encoding='utf-8')
   ```

3. Run the full code to train the models and generate stories.  

## **Output**
- Randomly generated Urdu sentences and paragraphs.  
- Top **starting words**, unigram, bigram, and trigram examples for validation.  

## **Example Output**
```text
Generated Story:
[Random Urdu paragraphs here]

Top Starting Words: ['word1', 'word2', ...]

Unigram Frequencies:
word1: 10
word2: 8

Bigrams:
word1: {'word2': 5, 'word3': 3}

Trigrams:
('word1', 'word2'): {'word3': 4, 'word4': 2}
```

## **Limitations**
- Sentences lack **semantic coherence** and often do not form meaningful narratives.  
- Improvements can be made using more advanced models like **LSTM** or **Transformers**.

## **Skills Applied**
- **Natural Language Processing (NLP)**  
- **N-Gram Language Models**  
- **Probability Distributions**  
- **Python Programming**  

---
