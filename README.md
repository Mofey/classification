# 📚 Book Recommendation Engine using KNN
## 🚀 Overview
This project implements a book recommendation system using the K-Nearest Neighbors (KNN) algorithm from sklearn.neighbors. Leveraging the Book-Crossings dataset, the engine recommends books based on user ratings using collaborative filtering techniques.

## 📂 Dataset
The dataset contains user-generated ratings for various books, along with book metadata such as titles and ISBNs.

## 🛠️ Data Preparation
To build a meaningful recommendation engine, several preprocessing steps were carried out:

- Filtering:
  - Removed users with fewer than 200 ratings.
  - Removed books with fewer than 100 ratings.
  This filtering reduces noise and sparsity in the dataset.

- Merging:
  - Ratings were merged with book metadata to map ISBN to  corresponding book titles.
- Pivot Table Construction:
A user-item matrix was created:
  - Rows: Book titles
  - Columns: User IDs
  - Values: Rating scores
  Missing ratings were filled with 0, making the matrix suitable for KNN analysis.

## 🧠 Algorithm
K-Nearest Neighbors (KNN)
  - Similarity Metric:
  Cosine distance was used to measure similarity between books.
  - Model Fitting:
  The KNN model was trained on the user-item matrix.
  - Recommendation Function:
  The function get_recommends(book_title):
    - Finds the top 5 books most similar to the given title (excluding itself).
    - Returns recommendations with similarity distances.

## 📐 Data Structures Used
- Pandas DataFrames: For data manipulation, filtering, and merging.
- NumPy Arrays: For numerical computations and model inputs.
- Python Lists: For storing and returning recommendations.

## 📈 Summary
This project demonstrates a simple yet effective approach to collaborative filtering using KNN:
- Data preprocessing ensures the model focuses on active users and popular books.
- Cosine similarity enables identification of books with similar rating patterns.
- Efficient data structures and algorithms make the system scalable and interpretable.

📌 Dependencies
- Python 3.x
- pandas
- numpy
- scikit-learn

Install dependencies with:
<pre>
```bash
pip install pandas numpy scikit-learn
</pre>

## 🧪 Usage Example
<pre>
```python
recommendations = get_recommends("The Hobbit")
print(recommendations)
</pre>

## 📎 License
This project is open-source and free to use under the [MIT License](https://mit-license.org/).