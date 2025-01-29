from collections import Counter

def calculate_similarity(user_purchases, all_users):
    """
    Calculates the similarity between a user and other users based on past purchases.
    """
    similarities = {}
    for user, purchases in all_users.items():
        similarity = len(set(user_purchases) & set(purchases))  # Number of common products
        similarities[user] = similarity
    return similarities

def predict_next_purchase(user_purchases, all_users, last_purchases):
    """
    Predicts the next purchase based on the nearest neighbor method.
    """
    similarities = calculate_similarity(user_purchases, all_users)
    closest_user = max(similarities, key=similarities.get)  # Find the user with the highest similarity
    return last_purchases.get(closest_user, "No prediction")

# Previous purchases for all users
user_data = {
    "Anna": ["boxing gloves", "Moby Dick novel", "headphones", "sunglasses", "coffee beans"],
    "David": ["t-shirt", "coffee beans", "coffee maker", "coffee beans", "coffee beans"],
    "Jonna": ["sunglasses", "running shoes", "t-shirt", "running shoes", "wool socks"],
    "Fredrik": ["2001: A Space Odyssey (dvd)", "headphones", "t-shirt", "boxing gloves", "sandals"],
    "Hanna": ["t-shirt", "sandals", "sunglasses", "Moby Dick novel"],
    "Leo": ["Moby Dick novel", "coffee beans", "2001: A Space Odyssey (dvd)", "headphones", "coffee beans"]
}

# Latest purchases per user
last_purchases = {
    "Anna": "coffee beans",
    "David": "coffee beans",
    "Jonna": "wool socks",
    "Fredrik": "sandals",
    "Hanna": "sunscreen",
    "Leo": "coffee beans"
}

# Maria's previous purchases
maria_purchases = ["green tea", "t-shirt", "sunglasses", "sandals"]

# Predict Maria's next purchase
next_purchase = predict_next_purchase(maria_purchases, user_data, last_purchases)
print(f"Expected next purchase for Maria: {next_purchase}")
