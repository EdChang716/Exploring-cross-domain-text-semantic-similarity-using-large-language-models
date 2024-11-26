# Exploring-cross-domain-text-semantic-similarity-using-large-language-models
This repository explores cross-domain text semantic similarity using large language models (LLMs). It includes an analysis of how text length impacts similarity metrics and evaluates the effectiveness of LLM-based embeddings in capturing semantic relationships across various domains. The project also addresses potential confounding factors and proposes methodologies for robust similarity measurement.

---

## Overview

The goal of this project is to analyze how LLM embeddings reflect semantic similarity across diverse domains, such as:
- Sports
- Finance
- Politics
- Beauty
- Medicine
- Arts
- Science

The analysis addresses key challenges, including:
1. Variability in text length (short, medium, and long texts).
2. Differences in semantic structures across domains.
3. Methodological considerations for accurate similarity measurement.

---

## Features
- **Cross-Domain Comparison**: Evaluates embeddings across texts from seven distinct domains.
- **Text Length Analysis**: Investigates the effect of text length (short: 40-80 words, medium: 120-250 words, long: 300-400+ words) on similarity scores.
- **Confounding Factors**: Explores how factors like domain-specific vocabulary or text structure influence similarity metrics.

---

## Getting Started

### Prerequisites
To run the project, ensure you have the following installed:
- Python 3.8+
- Required Python libraries (see `requirements.txt`)

### Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/Exploring-Cross-Domain-Text-Semantic-Similarity.git

## Dataset

The dataset consists of **35 news articles per domain**, with a total of 7 domains:

1. Sports  
2. Finance  
3. Politics  
4. Beauty  
5. Medicine  
6. Arts  
7. Science  

Each dataset contains texts of varying lengths:

- **Short Texts**: 40-80 words  
- **Medium Texts**: 120-250 words  
- **Long Texts**: 300-400+ words  

**Note**: Details on how to generate or access the dataset will be provided in the `data/` directory.

## Methodology

### Steps:

1. **Text Embedding Generation**  
   - Uses OpenAI's Ada-002 embedding model to generate high-dimensional vector representations for all texts.

2. **Similarity Measurement**  
   - Computes cosine similarity scores to quantify semantic similarity between text pairs.

3. **Analysis**  
   - Evaluates the relationship between text length and similarity metrics.  
   - Investigates the role of domain-specific language on embeddings.

---

### Tools & Libraries:
- Python 3.8+  
- OpenAI API  
- NumPy & Pandas for data manipulation  
- Matplotlib/Seaborn for visualization  

---

## Results

Key findings include:

- The semantic similarity of embeddings varies significantly across domains.
- Text length has a measurable impact on similarity scores, with shorter texts exhibiting greater variability.
- Confounding factors, such as domain-specific terminology, can influence embedding performance.

Detailed results and visualizations are available in the `results/` folder.

---

## Usage

### Running the Analysis

1. Prepare your API key for the OpenAI model.
2. Execute the notebook:
   ```bash
   jupyter notebook analysis.ipynb

### Example

Below is an example of how to compute text similarity using the Ada-002 embedding model:

```python
from openai.embeddings_utils import get_embedding, cosine_similarity

# Example texts
text1 = "The stock market rallied after the Federal Reserve announcement."
text2 = "Shares of tech companies surged due to investor optimism."

# Generate embeddings
embedding1 = get_embedding(text1, model="text-embedding-ada-002")
embedding2 = get_embedding(text2, model="text-embedding-ada-002")

# Compute similarity
similarity_score = cosine_similarity(embedding1, embedding2)
print(f"Similarity Score: {similarity_score}")
```

## Repository Structure
```plaintext

Exploring-Cross-Domain-Text-Semantic-Similarity/
├── data/                   # Dataset (if included)
├── notebooks/              # Jupyter notebooks for analysis
├── README.md               # Project description
└── LICENSE                 # License for the project
```

## Future Work

- Extend the analysis to additional domains.
- Experiment with other embedding models, such as BERT or Sentence Transformers.
- Investigate domain adaptation techniques to improve cross-domain similarity.

---

## Contributing

Contributions are welcome! If you have ideas for improvements or additional analyses, feel free to create a pull request or open an issue.


---

## Acknowledgments

- Special thanks to OpenAI for providing the Ada-002 model.
- Inspiration drawn from ongoing advancements in NLP and text similarity research.


