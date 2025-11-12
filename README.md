# Sentiment Analysis App

A compact Streamlit web app that demonstrates multiple approaches to sentiment and emotion analysis for text, images and IMDb movie reviews.

## What it does
- Text: Analyze sentiment and emotion from free-form user text using multiple libraries.
- IMDb movie reviews: Fetch reviews for a movie and analyze collective sentiment/emotions.
- Image: Detect faces in an uploaded image and estimate emotions per face and for the whole image.

## Key features
- Multiple sentiment engines: TextBlob, VADER (NLTK), Flair, text2emotion for richer comparisons.
- Image emotion detection with FER and OpenCV face detection.
- Simple multi-page Streamlit UI with a sidebar navigator and reusable modal components.
- Plotting and visualization using Plotly / Matplotlib and PIL for image handling.

## Project layout
- app.py — Streamlit entry point and page routing
- sidebar.py — Sidebar navigation and shared controls
- textPage.py — Text input UI and sentiment processing helpers
- imdbReviewsPage.py — IMDb review fetch + batch analysis UI
- imagePage.py — Image upload, face detection, image-level and per-face emotion analysis
- modals.py — Reusable modal dialogs and wrappers for sentiment/image libraries
- images/ — Static assets
- requirements.txt / packages.txt — Python dependencies

## Dependencies & Python version
- Python recommended: 3.8+ (some NLP/vision packages have limited wheels for newer versions)
- See requirements.txt for the full list (streamlit, flair, textblob, nltk, text2emotion, fer, opencv-python, pillow, plotly, pandas, requests, etc.)

## How it works 
- Text: input text → run multiple analyzers → normalize results → show label, scores and visualizations.
- IMDb: query movie → fetch reviews → batch-process with selected analyzers → aggregate and visualize sentiment distribution. ( 2 IMDb API requests per Analysis → 100 API calls per day Limit )
- Image: upload image → detect faces with OpenCV → run FER/emotion model per face and for full image → display bounding boxes and emotion charts.



