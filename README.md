# Pixelator

<img width="2392" alt="Architecture" src="https://github.com/Denish-Pasupuleti/Pixelator/assets/24259706/723fabe5-d6f0-4f86-9802-6de2268add90">

This project is to create a simple event-driven image processing pipeline. The pipeline uses two S3 buckets, a source bucket and a processed bucket. When images are added to the source bucket a lambda function is triggered based on the PUT. When invoked the lambda function receives the event and extracts the bucket and object information. Once those details are known, the lambda function, using the PIL module pixelates the image with 5 different variations (8x8, 16x16, 32x32, 48x48 and 64x64) and uploads them to the processed bucket.
