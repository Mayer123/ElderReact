# ElderReact: A Multimodal Dataset for Recognizing Emotional Response in Aging Adults
This repository contains annotations and features for the paper "ElderReact: A Multimodal Dataset for Recognizing Emotional Response in Aging Adults". See full paper [here](https://dl.acm.org/doi/10.1145/3340555.3353747)

ElderReact is a multimodal dataset for studying elders' emtional response. It contains 1,323 video clips of 46 individuals in total in which 26 are female and 20 are male. For each of the video clips, 6 basic emotions (Anger, Disgust, Fear, Happiness, Sadness, Surprise) and valence are annotated. For more information about the dataset, please refer to the paper: ElderReact: A Multimodal Dataset for Recognizing Emotional Response in Aging Adults. 

# Annotations
To obtain the labels for these videos, we hired crowd workers from Amazon Mechnical Turk and each video is annotated by 3 independent workers. All emotions are rated on 1-4 scale where 1 means the absence of emotion and 4 means the intense presence of emotion. Valence is rated on 1-7 scale where 1 means very negative and 7 means very position. We converted raw ratings of emotions into binary values by using 2 as the threshold, e.g [2,3,4] => 1 and [1] => 0. Then final labels are determined by majority voting of 3 workers. In annotation files, each line contain labels for one video and has following format: (1->filename, 2->Anger, 3->Disgust, 4->Fear, 5->Happiness, 6->Sadness, 7->Surprise, 8->Gender, 9->Valence).

# Videos
Our videos are available to public use for academic research purpose. If you would like to download the data, please fill out the form [here](https://docs.google.com/forms/d/e/1FAIpQLSd48fPwzEat0Ro6ZrPv2ezDfJz8C3mLoDFHyskJH-JUZr8TNA/viewform?usp=sf_link) and we will get back to you with instructions to download after receiving your request. Please make sure to use academia affiliated email when filling the form.

# Features
Visual features are extracted using the open-source tool OpenFace. We selected frames where the faces are successfully detected. Audio features are extracted using COVAREP, with frame length of 10 milliseconds. After extracting the
raw features for each frame, we summarize the video for both modalities by computing the mean and standard deviation for all frames and then concatenate them.
For building the model, we only used a subset of the features. For video features, we use gaze, gaze angle, pose and other features as described in baseline.py. For audio features, we only use the first 36 dimensions of mean and standard deviation respectively. 


## Cite 
```
@inproceedings{10.1145/3340555.3353747,
author = {Ma, Kaixin and Wang, Xinyu and Yang, Xinru and Zhang, Mingtong and Girard, Jeffrey M and Morency, Louis-Philippe},
title = {ElderReact: A Multimodal Dataset for Recognizing Emotional Response in Aging Adults},
year = {2019},
isbn = {9781450368605},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
url = {https://doi.org/10.1145/3340555.3353747},
doi = {10.1145/3340555.3353747},
booktitle = {2019 International Conference on Multimodal Interaction},
pages = {349–357},
numpages = {9},
keywords = {Emotion Recognition, elders, nonverbal behavior analysis},
location = {Suzhou, China},
series = {ICMI '19}
}
```
