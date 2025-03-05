<h1 align="center">Hybrid Book Recommendation System</h1>
<br/>

<h2>🚀 <strong>Objective</strong></h2>
<p>
    The goal of this project is to implement a book recommendation system using various machine learning methods, 
    including collaborative filtering (item-based and user-based), model-based techniques (SVD and KNN), 
    and content-based filtering. The final solution is a hybrid recommendation system that combines these 
    approaches to provide accurate and explainable book recommendations.
</p>

<h2>🛠 Technology Stack</h2>
<div class="badges">
    <img src="https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54" alt="Python"/>
    <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas"/>
    <img src="https://img.shields.io/badge/Scikit_learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-learn"/>
    <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy"/>
    <img src="https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=matplotlib&logoColor=white" alt="Matplotlib"/>
    <img src="https://img.shields.io/badge/Seaborn-3776AB?style=for-the-badge&logo=seaborn&logoColor=white" alt="Seaborn"/>
    <img src="https://img.shields.io/badge/Surprise-FF6F61?style=for-the-badge" alt="Surprise Library"/>
</div>

<h2>📂 <strong>Project Summary</strong></h2>
<p>
    This project demonstrates how to build a hybrid recommendation system by combining multiple machine learning 
    approaches. By leveraging the Goodreads dataset, the system provides personalized book recommendations while 
    addressing challenges such as data sparsity and the cold-start problem. The hybrid model achieves a Mean 
    Absolute Error (MAE) of 0.707 and ensures 79.4% of predictions are within 1 point of actual ratings.
</p>

<h2>📈 <strong>Methodology</strong></h2>
<table style="width:100%; border-collapse: collapse; margin-bottom: 20px;">
    <thead>
        <tr>
            <th style="background-color: #f2f2f2; border: 1px solid #ddd; padding: 8px;">Approach</th>
            <th style="background-color: #f2f2f2; border: 1px solid #ddd; padding: 8px;">Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="border: 1px solid #ddd; padding: 8px;">Collaborative Filtering</td>
            <td style="border: 1px solid #ddd; padding: 8px;">Implements item-based and user-based approaches to capture user preferences.</td>
        </tr>
        <tr>
            <td style="border: 1px solid #ddd; padding: 8px;">Model-Based Techniques</td>
            <td style="border: 1px solid #ddd; padding: 8px;">Utilizes SVD and KNN for matrix factorization and neighborhood-based predictions.</td>
        </tr>
        <tr>
            <td style="border: 1px solid #ddd; padding: 8px;">Content-Based Filtering</td>
            <td style="border: 1px solid #ddd; padding: 8px;">Uses book metadata (e.g., title, authors, publication year) to recommend similar books.</td>
        </tr>
        <tr>
            <td style="border: 1px solid #ddd; padding: 8px;">Hybrid Model</td>
            <td style="border: 1px solid #ddd; padding: 8px;">Combines all approaches with optimized weights to maximize accuracy and explainability.</td>
        </tr>
    </tbody>
</table>

<h2>🔍 <strong>Implementation Details</strong></h2>

<h3>📋 Data Preprocessing</h3>
<table style="width:100%; border-collapse: collapse; margin-bottom: 20px;">
    <thead>
        <tr>
            <th style="background-color: #f2f2f2; border: 1px solid #ddd; padding: 8px;">Step</th>
            <th style="background-color: #f2f2f2; border: 1px solid #ddd; padding: 8px;">Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="border: 1px solid #ddd; padding: 8px;">1</td>
            <td style="border: 1px solid #ddd; padding: 8px;">Loaded book metadata and ratings dataset. Original data size: (79,701, 7).</td>
        </tr>
        <tr>
            <td style="border: 1px solid #ddd; padding: 8px;">2</td>
            <td style="border: 1px solid #ddd; padding: 8px;">Filtered books with an average rating ≥ 2.0. Remaining: (36,110, 7).</td>
        </tr>
        <tr>
            <td style="border: 1px solid #ddd; padding: 8px;">3</td>
            <td style="border: 1px solid #ddd; padding: 8px;">Kept users with ≥ 5 ratings and books with ≥ 10 ratings.</td>
        </tr>
        <tr>
            <td style="border: 1px solid #ddd; padding: 8px;">4</td>
            <td style="border: 1px solid #ddd; padding: 8px;">Split into training (25,221, 4), validation (5,416, 7), and test (5,417, 7) sets.</td>
        </tr>
        <tr>
            <td style="border: 1px solid #ddd; padding: 8px;">5</td>
            <td style="border: 1px solid #ddd; padding: 8px;">Created user-item interaction matrix (sparsity: 0.9926).</td>
        </tr>
    </tbody>
</table>

<h3>📌 Developing Prediction Approaches</h3>
<ul>
    <li>Computed TF-IDF vectors and cosine similarity for content-based filtering.</li>
    <li>Generated item-based and user-based similarity matrices.</li>
    <li>Trained SVD (100 factors, 20 epochs) and KNN (k=40, Pearson) models.</li>
    <li>Each function returns a predicted rating and similar books/users for explainability.</li>
</ul>

<h3>📌 Evaluation of Different Recommendation Approaches</h3>
<table style="width:100%; border-collapse: collapse; margin-bottom: 20px;">
    <thead>
        <tr>
            <th style="background-color: #f2f2f2; border: 1px solid #ddd; padding: 8px;">Approach</th>
            <th style="background-color: #f2f2f2; border: 1px solid #ddd; padding: 8px;">MAE</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="border: 1px solid #ddd; padding: 8px;">Item-Based Filtering</td>
            <td style="border: 1px solid #ddd; padding: 8px;">0.662</td>
        </tr>
            <td style="border: 1px solid #ddd; padding: 8px;">Hybrid Model</td>
            <td style="border: 1px solid #ddd; padding: 8px;">0.707</td>        
        <tr>
            <td style="border: 1px solid #ddd; padding: 8px;">KNN</td>
            <td style="border: 1px solid #ddd; padding: 8px;">0.727</td>
        </tr>
        <tr>
            <td style="border: 1px solid #ddd; padding: 8px;">SVD</td>
            <td style="border: 1px solid #ddd; padding: 8px;">0.737</td>
        </tr>
        <tr>
            <td style="border: 1px solid #ddd; padding: 8px;">Content-Based Filtering</td>
            <td style="border: 1px solid #ddd; padding: 8px;">1.476</td>
        </tr>
        <tr>
        </tr>
    </tbody>
</table>

<h3>📌 Determining Hybrid Model Weights</h3>
<ul>
    <li>Calculated weights using inverse MAE scores and user preference distribution.</li>
    <li>Normalized weights to ensure balanced contribution from all approaches.</li>
    <li>Final weights determined by averaging MAE-based and user-based weights.</li>
    <li>Combines predictions from Item-based, User-based, Content-based, SVD, and KNN approaches.</li>
</ul>

<h3>📌 Comparing Actual vs Predicted Ratings</h3>
<ul>
    <li>Item-based filtering demonstrated the smallest overall error variance, making it the most reliable single approach.</li>
    <li>Hybrid model provided a stable balance between different models, ensuring adaptability to various user behaviors.</li>
    <li>Content-based filtering had the highest error, indicating its struggle with generalization.</li>
</ul>

<h2>📊 <strong>Key Improvements</strong></h2>
<ul>
    <li><strong>Accuracy:</strong> Achieved a Mean Absolute Error (MAE) of 0.707 and Root Mean Squared Error (RMSE) of 0.903.</li>
    <li><strong>Explainability:</strong> Provides transparent explanations for recommendations, including similar books and user preferences.</li>
    <li><strong>Handling Sparse Data:</strong> Effectively manages 99% data sparsity using advanced techniques.</li>
    <li><strong>Scalability:</strong> The hybrid model can be extended to larger datasets and real-time applications.</li>
</ul>

<h2>🔍 <strong>Implementation Workflow</strong></h2>
<ol>
    <li>Loaded and preprocessed the Goodreads dataset.</li>
    <li>Implemented and evaluated multiple recommendation approaches.</li>
    <li>Determined optimal weights for the hybrid model based on performance.</li>
    <li>Tested the hybrid model on the test set and analyzed prediction accuracy.</li>
    <li>Generated personalized and explainable recommendations for users.</li>
</ol>

<h2>📚 <strong>Dataset</strong></h2>
<p>
    The project utilizes the <strong>Goodbooks-10k</strong> dataset available on Kaggle. This dataset contains 
    information on 10,000 books from Goodreads, including book metadata (e.g., titles, authors, publication year) 
    and approximately 6 million user ratings. It is an ideal resource for building and testing recommendation systems 
    due to its comprehensive coverage and real-world applicability.
</p>
<ul>
    <li><strong>Source:</strong> <a href="https://www.kaggle.com/datasets/zygmunt/goodbooks-10k">Goodbooks-10k on Kaggle</a></li>
    <li><strong>Contents:</strong> Book metadata and user ratings</li>
    <li><strong>Size:</strong> 10,000 books, ~6 million ratings</li>
    <li><strong>License:</strong> CC0: Public Domain</li>
</ul>

<h2>📢 <strong>Conclusion</strong></h2>
<p>
    The project successfully implemented a hybrid book recommendation system that combines multiple machine 
    learning approaches to provide accurate and explainable recommendations. Key learnings include the 
    effectiveness of item-based filtering, the balanced performance of the hybrid model, and the challenges 
    of content-based filtering.
</p>

<h2>Connect With Me</h2>
<div align="center">
    <a href="https://www.linkedin.com/in/ecembayindir/" target="_blank">
        <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
    </a>
    <a href="mailto:ecmbyndr@gmail.com">
        <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/>
    </a>
</div>
<br>
<p align="center">© 2025 Ecem Bayındır. All rights reserved.</p>
<hr/>
<p align="center">
    <img src="https://komarev.com/ghpvc/?username=ecembayindir&repo=Hybrid-Book-Recommendation-System&label=Repository%20views&color=0e75b6&style=flat" alt="Repository Views">
</p>
