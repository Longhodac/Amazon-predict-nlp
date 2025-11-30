# Spotify Tracks Dataset

This dataset contains Spotify tracks spanning approximately 125 genres. Each row corresponds to a single track and includes audio features and metadata. The data is provided in CSV (tabular) format and can be loaded quickly with pandas.

**Highlights:**

- Tracks: (varies per file)
- Genres covered: ~125

## Usage

Common uses for this dataset:

- **Recommendation systems:** Build personalized or content-based recommenders using audio features and metadata.
- **Classification:** Predict genres or other labels from audio features.
- **Exploratory analysis / visualization:** Analyze feature distributions, correlations, and trends across genres.
- **Feature engineering / modeling practice:** Use as a dataset for ML exercises and benchmarking.

## Column Descriptions

Below are the main columns and a short description for each. Use these when preparing the data for modeling or analysis.

- **track_id:** The Spotify ID for the track.
- **artists:** The performing artists' names. Multiple artists are separated by a `;`.
- **album_name:** The album in which the track appears.
- **track_name:** The name of the track.
- **popularity:** Integer 0–100 indicating track popularity (higher = more popular). Derived from number and recency of plays; duplicate tracks are rated independently.
- **duration_ms:** Track length in milliseconds.
- **explicit:** Boolean indicating whether the track contains explicit lyrics (`true` or `false`).
- **danceability:** Float 0.0–1.0 describing suitability for dancing (higher = more danceable).
- **energy:** Float 0.0–1.0 measuring perceived intensity and activity (higher = more energetic).
- **key:** Integer mapping to musical pitch (Pitch Class). Example: 0 = C, 1 = C♯/D♭, etc.; `-1` indicates no key detected.
- **loudness:** Overall loudness in decibels (dB).
- **mode:** Indicates modality of the track (1 = major, 0 = minor).
- **speechiness:** Float 0.0–1.0 detecting presence of spoken words (higher values indicate more speech-like content).
- **acousticness:** Float 0.0–1.0 confidence of the track being acoustic (1.0 = highly acoustic).
- **instrumentalness:** Float predicting whether track contains no vocals (values closer to 1.0 indicate instrumental tracks).
- **liveness:** Float indicating presence of an audience (values > 0.8 suggest live recording).
- **valence:** Float 0.0–1.0 describing musical positiveness (higher = more positive/cheerful).
- **tempo:** Estimated tempo in beats per minute (BPM).
- **time_signature:** Estimated time signature (typically 3–7).
- **track_genre:** Genre label for the track.

## Notes & Tips

- Missing values: Check `duration_ms`, `key`, and feature columns for missing or placeholder values (e.g., `-1` for unknown key).
- Preprocessing: Consider normalizing numeric features and handling class imbalance when training classifiers.
- Combining artists: If you need a single artist field, decide how to handle multiple artists (e.g., take the first, explode rows, or keep as list).

If you'd like, I can also:

- Add a small `README.md` with example loading code (`pandas.read_csv`) and a quick usage snippet.
- Convert the column descriptions into a markdown table for easier scanning.
