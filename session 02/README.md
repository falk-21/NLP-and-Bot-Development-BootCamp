# Session 02 — NLP EDA Notebook & Dataset

This folder contains the exploratory data analysis (EDA) materials for Session 02 of the NLP and Bot Development BootCamp.

## Files

- `NLP_(EDA).ipynb`
  - Interactive Jupyter/Colab notebook that performs EDA on the reviews dataset.
  - Key analyses included:
    - Data loading and basic dataframe inspection (shape, dtypes, missing values)
    - Class distribution (positive / negative) and visualizations (bar plot, pie chart)
    - Text-length features: Character_Count, Word_Count, Sentence_Count
    - Tokenization and stopword handling using NLTK
    - Word cloud generation and common n-gram counts
    - Example plots with matplotlib / seaborn
  - Notes: the notebook includes Colab-specific upload helpers; it will also run in a local Jupyter environment after installing required packages and ensuring the dataset filename matches what the notebook expects.

- `reviews  2.csv`
  - Original CSV dataset used by the notebook. Contains ~56,000 rows of reviews.
  - Expected columns (as used in the notebook): `rating` (values like `positive` / `negative`) and `review` (text).
  - Note: the filename includes two spaces before the `2` in this repository. If you prefer a cleaner name, consider renaming to `reviews.csv` and updating any notebook cells that reference the filename.

## Quick start (run the notebook)

1. Install dependencies (if running locally):

```
pip install pandas numpy matplotlib seaborn nltk wordcloud
```

2. In Python / notebook, download required NLTK data (the notebook already runs these calls):

```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
```

3. Open `NLP_(EDA).ipynb` in Jupyter or Colab. If using Colab, you can upload `reviews  2.csv` (or your renamed CSV) when prompted by the upload cell.

4. Run the cells top-to-bottom. The notebook will create new dataframe columns like `Character_Count`, `Word_Count`, and `Sentence_Count` and will generate plots and wordclouds.

## Notes & recommendations

- Dataset size: ~56k rows — some plotting or heavy operations (e.g., full wordcloud on all text) may take time in limited environments.
- Filenames with spaces can cause inconvenience in scripts — consider renaming `reviews  2.csv` to `reviews.csv` and updating the notebook accordingly.
- If you plan to extend the notebook, suggested next steps:
  - Add a preprocessing cell that normalizes text (lowercasing, punctuation removal, lemmatization)
  - Save intermediate cleaned datasets to `data/` (create a `data/` folder)
  - Add a reproducible requirements file (requirements.txt) or a Conda environment file

## Contact
If you have questions about the notebook or dataset, open an issue in this repository or reach out to the repository owner.
