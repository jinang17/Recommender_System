Applied Aging:
The dataset contained reviews spread across different years. To give more importance to recent reviews, we introduced a factor that decreases as reviews get older. We multiplied this factor with the latest rating to create a new overall rating. This approach considers both the time of review and the ratings themselves.

Applied Matrix Factorization to the User-Item Matrix:
Dealing with large user-product matrices is a challenging aspect of recommendation systems. To tackle this, we turned to a technique known as Matrix Factorization, with a specific focus on Singular Value Decomposition (SVD). SVD stands out as a robust choice due to its ability to handle sparse matrices effectively.

SVD's significance lies in its capacity to capture latent factors within the data. This means that instead of directly working with the original data points, we uncover hidden features or factors that drive the interactions between users and items. In our case, these factors influence user preferences and item characteristics that contribute to ratings.

The assumption of a smaller number of latent factors allows SVD to offer dimensionality reduction. By mapping users and items into a lower-dimensional space, the computational complexity is reduced, leading to faster and more efficient calculations. Unlike other methods like Principal Component Analysis (PCA), SVD is tailor-made for collaborative filtering, which is a powerful technique for personalized recommendations in systems like ours.

Another notable advantage of SVD is its ability to handle missing data gracefully. In recommendation systems, where not all users rate all items, SVD can predict missing ratings by estimating them from the latent factors it has learned. This predictive ability helps enhance the quality of recommendations and fill in the gaps in the user-item matrix.

Furthermore, we've incorporated regularization techniques to prevent overfitting. These techniques introduce a penalty term that encourages the model to generalize well to new, unseen data, making our recommendations more robust and accurate.

To fine-tune our model, we've introduced bias terms. These terms adjust the predictions based on average ratings of items and users, correcting the discrepancies between predicted and actual values.

In summary, by employing SVD and matrix factorization, we've harnessed the power of latent factors, efficient dimensionality reduction, handling missing data, and regularization. This comprehensive approach enables us to provide high-quality recommendations by capturing intricate patterns within the user-item interactions. To determine the top K recommendations, we trained the model, predicted ratings for unrated items, and selected the highest-rated items for the user.
