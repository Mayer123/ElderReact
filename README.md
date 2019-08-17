# ElderReact
ElderReact is a multimodal dataset for studying elders' emtional response. It contains 1,323 video clips of 46 individuals in total in which 26 are female and 20 are male. For each of the video clips, 6 basic emotions (Anger, Disgust, Fear, Happiness, Sadness, Surprise) and valence are annotated. For more information about the dataset, please refer to the paper: ElderReact: A Multimodal Dataset for Recognizing Emotional Response in Aging Adults. 

# Annoatations
To obtain the labels for these videos, we hired crowd workers from Amazon Mechnical Turk and each video is annotated by 3 independent workers. All emotions are rated on 1-4 scale where 1 means the absence of emotion and 4 means the intense presence of emotion. Valence is rated on 1-7 scale where 1 means very negative and 7 means very position. 

# Videos
Our videos are available to public use for academic research purpose. If you would like to download the data, please fill out the form here and we will get back to you with instructions to download after receiving your request. Please make sure to use academia affiliated email when filling the form.

# Features
Visual features are extracted using the open-source tool OpenFace. We selected frames where the faces are successfully detected. Audio features are extracted using COVAREP, with frame length of 10 milliseconds. After extracting the
raw features for each frame, we summarize the video for both modalities by computing the mean and standard deviation for all frames and then concatenate them.