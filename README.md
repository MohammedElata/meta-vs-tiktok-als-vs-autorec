# Meta vs TikTok: ALS vs AutoRec Recommender Systems

MSc Data Analytics dissertation comparing two recommender-system approaches under the same experimental conditions:

* **Meta-inspired approach:** Alternating Least Squares (ALS) matrix factorisation
* **TikTok-inspired approach:** AutoRec, an autoencoder-based deep-learning recommender

The study uses the **MovieLens 100K** dataset as a proxy for social-media interaction data. It does not use or reproduce Meta or TikTok’s proprietary data or algorithms.

## Research Aim

To compare matrix factorisation and deep learning in recommendation systems, assessing the trade-off between predictive accuracy, ranking quality, catalogue coverage and recommendation diversity.

## Methodology

* **Dataset:** MovieLens 100K - 100,000 ratings, 943 users and 1,682 items
* **Models:** ALS matrix factorisation and AutoRec
* **Evaluation:** RMSE, Precision@10, Recall@10, NDCG@10, Coverage and Diversity
* **Context:** Interpretation of findings through the different recommender-system strategies associated with Meta and TikTok

## Results

| Metric       | ALS Matrix Factorisation | AutoRec Deep Learning |
| ------------ | -----------------------: | --------------------: |
| RMSE         |                   3.2916 |            **1.1732** |
| Precision@10 |               **0.2344** |                0.0413 |
| Recall@10    |               **0.1601** |                0.0359 |
| NDCG@10      |               **0.2794** |                0.0392 |
| Coverage     |                **0.384** |                 0.211 |
| Diversity    |                **0.907** |                 0.102 |

## Key Findings

* **AutoRec achieved lower RMSE**, indicating better rating-prediction accuracy in this experiment.
* **ALS achieved stronger ranking performance, coverage and diversity**, indicating more effective top-item recommendations under the study's evaluation setup.
* The findings show why recommender systems should not be evaluated by predictive accuracy alone: the appropriate approach depends on the product objective, dataset scale and desired user experience.
* AutoRec's weaker ranking results suggest that larger, richer interaction datasets are important for deep-learning recommendation models to generalise effectively.

## Tools

* **Programming:** Python
* **Data Processing:** Pandas, NumPy and SciPy
* **Machine Learning:** Scikit-learn and Implicit
* **Deep Learning:** PyTorch
* **Visualisation:** Matplotlib
* **Development:** Jupyter Notebook, Google Colab, Git and GitHub

## Repository Structure

```text
meta-vs-tiktok-als-vs-autorec/
├── notebooks/
│   └── meta_vs_tiktok_recommender_comparison.ipynb
├── .gitignore
├── README.md
└── requirements.txt
```

## View the Project

[Open the complete ALS and AutoRec comparison notebook](notebooks/meta_vs_tiktok_recommender_comparison.ipynb)

The notebook contains the complete workflow:

1. Environment setup and reproducibility controls
2. Automatic MovieLens 100K download
3. Data preparation and user-item mapping
4. Multi-metric evaluation framework
5. ALS matrix-factorisation implementation
6. AutoRec deep-learning implementation
7. Comparative results and visualisations
8. Training diagnostics

## Running the Project

### Google Colab

Open the notebook using its **Open in Colab** button and select **Runtime → Run all**. The MovieLens 100K dataset downloads automatically.

### Local Environment

```bash
git clone https://github.com/MohammedElata/meta-vs-tiktok-als-vs-autorec.git
cd meta-vs-tiktok-als-vs-autorec
pip install -r requirements.txt
jupyter notebook notebooks/meta_vs_tiktok_recommender_comparison.ipynb
```

## Limitations

* MovieLens 100K is a movie-rating dataset used as a proxy for social-media interactions.
* The study does not reproduce Meta or TikTok's proprietary recommendation algorithms.
* The AutoRec model is constrained by the size and sparsity of the available dataset.
* Results demonstrate model trade-offs within this controlled experimental setup and should not be treated as direct platform-performance comparisons.

## Future Work

Future development could explore larger implicit-feedback datasets, Neural Collaborative Filtering, sequential recommenders, graph neural networks and hybrid architectures combining the strengths of ALS and AutoRec.
