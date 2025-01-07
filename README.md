# Food Recommendation System

This repository contains the implementation of a **Food Recommendation System** designed to provide personalized food suggestions based on user preferences, nutritional needs, and collaborative filtering techniques. The system leverages content-based and collaborative filtering algorithms to offer tailored recommendations for both new and existing users.

## Table of Contents
- [Introduction](#introduction)
- [Key Features](#key-features)
- [Dataset](#dataset)
- [Recommendation Techniques](#recommendation-techniques)
- [Core Algorithms](#core-algorithms)
- [Recommendation Logic](#recommendation-logic)
- [Evaluation Metrics](#evaluation-metrics)
- [Results](#results)
- [Future Directions](#future-directions)
- [Contributors](#contributors)

## Introduction
The Food Recommendation System addresses the challenges of culinary diversity, information overload, and the growing demand for personalized food suggestions. By combining content-based and collaborative filtering techniques, the system provides users with tailored recommendations that align with their tastes, dietary goals, and preferences.

## Key Features
- **Personalized Recommendations**: Tailored food suggestions based on individual user preferences and nutritional needs.
- **Top-Rated Recipes**: Recommendations of the highest-rated recipes using collaborative filtering.
- **Nutrition-Based Recommendations**: Recipes suggested based on nutritional preferences and dietary goals.
- **Enhanced User Experience**: Simplified decision-making tools to improve user satisfaction.

## Dataset
The system uses a dataset composed of four key files:
1. **pp_recipes**: Contains comprehensive information about recipes.
2. **pp_users**: Contains user-related data.
3. **raw_interactions**: Records user interactions with recipes.
4. **raw_recipes**: Provides detailed information about recipes.

### Data Preprocessing
- **Cleaning and Filtering**: Irrelevant columns and duplicates are removed. Users with fewer than 10 interactions are filtered out to ensure data quality.
- **Data Transformation**: Nutritional information is split, columns are normalized, and user and recipe IDs are mapped to continuous indices.
- **Matrix Creation**: A sparse matrix is developed to efficiently store user ratings and interactions.

## Recommendation Techniques
The system offers different recommendation strategies for new and existing users:
- **New Users**:
  - Nutrient-Based Recommendations using content-based filtering.
  - Top-Rated Recipes leveraging collaborative filtering.
- **Existing Users**:
  - Personalized Nutrient-Based Recommendations.
  - Preference-Based Recommendations using collaborative filtering with K-Nearest Neighbors (KNN).

## Core Algorithms
The system relies on the following core algorithms:
- **Content-Based Filtering (Cosine Similarity)**: Measures similarity between items or user profiles by calculating the cosine of the angle between two vectors representing their features.
- **K-Nearest Neighbors (KNN)**: Identifies nearest neighbors based on similarity metrics, ensuring recommendations are derived from similar users or items.
- **Collaborative Filtering**: Utilizes user behavior and preferences to make recommendations by finding patterns in user-item interactions.

## Recommendation Logic
The recommendation process follows these steps:
1. **ID Mapping**: Maps user and recipe IDs to continuous indices for efficient processing.
2. **Approximate Nearest Neighbors**: Utilizes KNN to find similar users based on preferences and interactions.
3. **Top-Rated Recommendations**: Suggests highest-rated recipes using collaborative filtering techniques.
4. **Nutrition-Based Recommendations**: Recommends recipes based on nutritional preferences and dietary goals.
5. **Similarity-Based Recommendations**: Suggests recipes based on ratings from similar users identified through KNN.

## Evaluation Metrics
The system's performance is evaluated using the following metrics:
- **MAE (Mean Absolute Error)**: Measures the average magnitude of errors in predictions.
- **RMSE (Root Mean Squared Error)**: Emphasizes larger errors in the model.
- **F1-Score**: Harmonic mean of precision and recall, balancing both metrics.
- **Mean Rating**: Average predicted rating, indicating overall positive recommendations.

## Results
The system demonstrates effective personalized food recommendations with the following performance metrics:
- **MAE**: 0.9119
- **RMSE**: 1.3932
- **F1-Score**: 0.9322
- **Mean Rating**: 4.37

## Future Directions
- **Enhanced User Experience**: Improved UI and real-time updates.
- **Advanced Filtering**: More sophisticated content-based and collaborative filtering techniques.
- **Data Integration**: Incorporating more diverse data sources.
- **Personalization**: Deeper understanding of individual preferences.

## Contributors
- Hager Tamer AbdAlfattah
- Aya Elsheshtawy Mansoub Elbereky
- Noura Moustafa Maklad

---

For more details, refer to the [Food-Recommendation-System.pdf](Food-Recommendation-System.pdf) file in this repository.
