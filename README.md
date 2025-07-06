# HybridFlix: A Hybrid Movie Recommendation System
A sophisticated hybrid movie recommendation system that combines content-based and collaborative filtering approaches to deliver personalized movie suggestions. The system addresses common challenges in recommendation systems such as cold start problems and data sparsity while maintaining high accuracy and diversity.

## 🎯 Key Features

- **Hybrid Approach**: Combines content-based and collaborative filtering for superior recommendations
- **Advanced Text Processing**: Utilizes TF-IDF vectorization and cosine similarity for content analysis
- **Bayesian Rating System**: Implements weighted ratings to handle popularity bias
- **Comprehensive Evaluation**: Measures performance using diversity, novelty, and NDCG metrics
- **Scalable Architecture**: Built with Python and optimized for large-scale datasets
- **Real-time Processing**: Designed for responsive recommendation generation

## 📊 System Architecture

The HybridFlix system consists of three main components:

1. **Content-Based Recommender**: Analyzes movie features (genres, keywords, overviews) using TF-IDF vectorization
2. **Collaborative Filtering**: Leverages user interaction patterns and rating matrices
3. **Hybrid Model**: Dynamically combines both approaches with weighted scoring

## 🛠️ Technologies Used

- **Python**: Core programming language
- **Pandas**: Data manipulation and analysis
- **Scikit-learn**: Machine learning algorithms and TF-IDF vectorization
- **NumPy**: Numerical computing
- **Matplotlib/Seaborn**: Data visualization
- **Jupyter Notebook**: Development environment

## 📈 Performance Metrics

The system is evaluated using multiple metrics:

- **Similarity**: Measures recommendation relevance
- **Diversity**: Assesses genre variety in recommendations
- **Novelty**: Evaluates the discovery of less popular movies
- **NDCG**: Normalized Discounted Cumulative Gain for ranking quality

## 🚀 Getting Started

### Prerequisites

```bash
Python 3.7+
pip (Python package manager)
```

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/hybridflix.git
cd hybridflix
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

3. Download the TMDB dataset:
   - Visit [TMDB Movie Metadata on Kaggle](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)
   - Download and place the dataset in the `data/` directory

### Usage

1. Launch Jupyter Notebook:
```bash
jupyter notebook
```

2. Open the main notebook file and run the cells sequentially

3. The system will process the data and generate recommendations based on your input

### Example Usage

```python
# Get recommendations for a specific movie
movie_title = "The Dark Knight"
recommendations = hybrid_recommender.get_recommendations(movie_title, n_recommendations=10)
print(recommendations)
```

## 📊 Results

The hybrid system demonstrates balanced performance across all evaluation metrics:

- **Content-Based**: High similarity scores but limited diversity
- **Collaborative Filtering**: Excellent diversity and novelty scores
- **Hybrid Model**: Optimal balance between accuracy and diversity

### Sample Recommendations for "The Dark Knight"

| Approach | Top Recommendations | Similarity Score |
|----------|-------------------|------------------|
| Content-Based | The Dark Knight Rises | 0.6805 |
| Collaborative | Inception | 0.9998 |
| Hybrid | The Dark Knight Rises | 0.6000 |

## 🔧 System Components

### Data Processing
- **Feature Engineering**: Combines movie overviews, keywords, and genres
- **Weighted Features**: Keywords (2x weight), Genres (3x weight)
- **Bayesian Rating**: Normalizes ratings based on vote counts and popularity

### Recommendation Algorithms
- **TF-IDF Vectorization**: Converts text features to numerical vectors
- **Cosine Similarity**: Measures similarity between movies and users
- **Dynamic Weighting**: Balances content and collaborative components

### Evaluation Framework
- **Diversity Calculation**: Counts unique genres in recommendations
- **Novelty Assessment**: Measures average popularity of recommended movies
- **NDCG Computation**: Evaluates ranking quality with relevance consideration

## 🎯 Future Enhancements

- **Deep Learning Integration**: Implement neural networks for complex pattern recognition
- **Sentiment Analysis**: Incorporate user review sentiment for enhanced recommendations
- **Real-time Processing**: Implement streaming data processing with Apache Spark
- **Multi-modal Support**: Add support for movie posters and trailers
- **A/B Testing Framework**: Implement systematic evaluation of recommendation strategies



## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- The Movie Database (TMDB) for providing the dataset
- Open source community for various libraries and tools
