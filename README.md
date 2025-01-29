# 🛍️ Nearest Neighbor Purchase Predictor

This project implements a nearest neighbor recommendation system to predict a user's next purchase based on past shopping behavior. It uses similarity between users by comparing their previous purchases.

# 📌 How It Works

The script calculates similarity between users by counting common previous purchases.
It finds the most similar user to the target user (Maria in this case).
It predicts the next purchase for the target user based on the most similar user's latest purchase.

# 🚀 Usage

Simply run the script, and it will output the predicted next purchase for Maria:
python recommendation_knn.py

# Example Output:
Expected next purchase for Maria: sunscreen

# 🛠️ Technologies Used

Python 3
Dictionary-based similarity comparison

# 📂 Files

recommendation_knn.py – The main script containing the recommendation algorithm.
"k-Nearest Neighbors" (kNN)

# 🎯 Future Improvements

Use cosine similarity or Jaccard index for better recommendation accuracy.
Implement a machine learning-based approach for more complex datasets.
Create a web API for real-time predictions.
