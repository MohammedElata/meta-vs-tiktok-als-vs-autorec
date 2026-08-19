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

Python, Pandas, NumPy, PyTorch, Scikit-learn, Matplotlib and Jupyter Notebook.

## Repository Structure

The implementation, reproducible notebooks, evaluation outputs and visualisations will be added to this repository.
