# Music Recommendation System

This is a music recommendation system built on top of the AudioSet dataset and the MAX-Audio-Embedding-Generator.

## Getting Started

### Prerequisites
- Downloaded audio dataset from AudioSet.

### Steps to Run

1. **Download Audio Data**:
   - Go to [AudioSet](https://research.google.com/audioset/).
   - Scroll down to the section titled "Manually download".
   - Download the compressed `tar.gz` file.
   - Double-click to uncompress the file in your project repository. These are YouTube videos that have been encoded using the MAX-Audio-Embedding-Generator.

2. **Process Audio Data**:
   - Run all cells in the `Spotify recommender.ipynb` notebook. This will:
     - Ensure extraction of only music audio.
     - Cut audio samples to 10 seconds each.
     - Store the processed data in a list of JSON for later use.

3. **Generate Recommendations**:
   - Run all cells in the `Annoy.ipynb` notebook. This notebook utilizes the nearest neighbor algorithm, ANNOY, to take an input audio sample and return a list of recommendations from our dataset.

## Embedding Generation (Optional)

While not necessary for the main project, these steps offer a deeper understanding of how embeddings are generated from raw `.wav` files.

### Steps:

1. **Run Locally**:
   - Follow the "Run Locally" instructions to build and start the Docker app.
   - The app should now be accessible at [http://localhost:5000](http://localhost:5000). Navigate to this URL in your browser to access the UI.

2. **Test Embedding Generation**:
   - Play around by uploading a `.wav` file through the UI and observe the generated embedding at the output.

3. **Embedding Conversion**:
   - Navigate to the `demo.ipynb` notebook. This notebook contains code to convert a `.wav` file into its embeddings by making a call to the Audio Embedding service.

