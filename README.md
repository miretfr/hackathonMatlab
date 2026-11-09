# Hiking Fitness Tracker

A MATLAB fitness tracker for hikers. Smartphone sensor data (GPS, accelerometer, altimeter) recorded with the MATLAB Mobile app is used to classify the type of physical activity and compute hike metrics: distance, steps, time spent, elevation gain and calories burned.

## Data

Recorded with MATLAB Mobile during sitting, walking and running. The accelerometer logs are labelled by activity and used to train the classifier.

## How it works

1. **Train and classify:** a classifier trained on labelled accelerometer data (sitting, walking, running) predicts the activity of an unknown recording.
2. **User input:** weight, height, gender and hiking frequency.
3. **Calculate:**
   - distance, summed between consecutive GPS points
   - steps, estimated from distance and an average stride of 2.5 ft
   - duration and elevation gain
   - calories, from an estimated MET value (based on speed and climbing rate), weight and duration
4. **Display:** activity pie chart, hiking path on a topographic map, elevation profile and speed over time.

## Run

Requires MATLAB with the Mapping Toolbox and the Statistics and Machine Learning Toolbox. Place `ExampleData.mat`, `ActivityLogs.mat` and `TRAINEDMODEL.mat` in the working folder, then run:
