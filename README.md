# mlnd-p6-capstone

### Udacity MLND Project 6 - Capstone Project

This is my submission for Project 6 - the final project on Udacity's Machine Learning Engineer Nanodegree.

The project brief asked the student to draw on what they'd learned throughout the Nanodegree program to solve a problem of their choice by applying machine learning algorithms and techniques. The project was designed to emulate the full machine learning development process, comprising dataset sourcing, proposal submission, development work and the compilation of a final report.

I chose to investigate whether it was possible to predict enjoyment of any given song using data from Spotify and Last.fm, ultimately developing an XGBoost classification model with accuracy of 63.6% and precision of 63.9%. 

### Install

This project requires Python 2.7 and the following Python libraries installed:
* [NumPy](http://www.numpy.org/)
* [Pandas](http://pandas.pydata.org/)
* [SciPy](https://www.scipy.org/)
* [matplotlib](https://matplotlib.org/)
* [seaborn](https://seaborn.pydata.org/)
* [scikit-learn](http://scikit-learn.org/stable/)
* [XGBoost](http://xgboost.readthedocs.io/en/latest/)

You will also need to have software installed to run and execute a [Jupyter Notebook](https://jupyter.org/).

### Code

The necessary Python code required to run the project is contained entirely within the `MLND Capstone Workflow.ipynb` notebook file. The underlying data is provided in the `markbannister_tracks_master.csv` file.

### Data

The dataset consists of 10,832 tracks and 15 potential predictor variables. This comprises over 11 years of my personal music listening history (as tracked by Last.fm), together with musical analysis of each track (as developed by [Spotify](https://developer.spotify.com/web-api/get-audio-features/)).

The full list of columns is as follows (note full descriptions of Spotify variables [here](https://developer.spotify.com/web-api/get-several-tracks/) and [here](https://developer.spotify.com/web-api/get-audio-features/)):

* Track: track name (Last.fm).
* Artist: artist name (Last.fm).
* Album: album name (Last.fm).
* First_played: datetime of first play (Last.fm).
* Last_played: datetime of most recent play (Last.fm).
* Play_count: total plays recorded (Last.fm).
* Days_in_library: total days since first play (Last.fm).
* Plays_per_year: Play_count / Days_in_library * 365.
* uri: the Spotify URI for the track. (Spotify).
* explicit: Whether or not the track has explicit lyrics (Spotify).
*	name: track name (Spotify).
* popularity: the popularity of the track. The value will be between 0 and 100, with 100 being the most popular. (Spotify).
* acousticness: confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic. (Spotify).
* analysis_url: an HTTP URL to access the full audio analysis of this track (Spotify).
* danceability: describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable (Spotify).
* duration_ms: the duration of the track in milliseconds (Spotify).
* energy: a measure from 0.0 to 1.0 representing a perceptual measure of intensity and activity (Spotify).
* id: the Spotify ID for the track (Spotify).
* instrumentalness: predicts whether a track contains no vocals. "Ooh" and "aah" sounds are treated as instrumental in this context. Rap or spoken word tracks are clearly "vocal". The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content (Spotify).
* key: the key the track is in (Spotify).
* liveness: detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live (Spotify).
* loudness: the overall loudness of a track in decibels (dB). Loudness values are averaged across the entire track and are useful for comparing relative loudness of tracks (Spotify).
* mode: indicates the modality (major or minor) of a track, the type of scale from which its melodic content is derived (Spotify).
* speechiness: detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value (Spotify).
* tempo: overall estimated tempo of a track in beats per minute (BPM) (Spotify).
* time_signature: estimated overall time signature of a track. The time signature (meter) is a notational convention to specify how many beats are in each bar (or measure) (Spotify).
* valence: a measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry) (Spotify).