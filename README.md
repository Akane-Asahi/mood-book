# Moodbook - A Mood-Based Book Recommender

This project is a semantic search system that recommends books based on a user's current mood. It uses natural language processing (NLP) to understand vague emotional input and suggest relevant book titles after clarifying the type of emotional state.

## Features

- Understands vague mood descriptions like "I'm feeling down" or "I feel broken"
- Asks the user to clarify if they meant mentally, spiritually, physically, etc.
- Suggests a book tailored to the confirmed emotional state
- Built using sentence-transformers for semantic matching
- Ready-to-run in Google Colab with a CSV-based dataset

## Dataset

The dataset `mood_book_recommender_dataset.csv` contains over 1,000 entries with:
- `user_input`: A vague mood-related sentence
- `mood_type`: One of several categories (e.g., mentally, emotionally, spiritually)
- `book`: A relevant book for that emotional state

You can easily extend the dataset by adding more examples or book recommendations.

## How It Works

1. The user inputs a vague mood (e.g., "I feel anxious").
2. The model computes semantic similarity between the input and dataset entries.
3. The most similar mood type is selected and suggested to the user.
4. The user confirms or changes the mood type.
5. A random book is recommended from the matching category.

## Setup Instructions

1. Clone this repository or open the Colab script directly.
2. Upload both `mood_book_recommender_dataset.csv` and `mood_book_colab.py` to your Colab environment.
3. Run the notebook and follow the instructions in the script.

## Dependencies

- Python 3.7+
- pandas
- torch
- sentence-transformers

Install dependencies using:

```bash
pip install -q sentence-transformers pandas torch
