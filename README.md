# vietnamese-voice-dataset
A Vietnamese voice dataset for text-to-speech (TTS) and automatic speech recognition (ASR) application

## Introduction
We present a Vietnamese voice dataset for text-to-speech (TTS) application. 
The dataset contains 619 hours of speech data, which is recorded by a southern vietnamese female speaker. 
This dataset is recorded in a controlled environment with professional recording tools. 
The dataset is available for research purpose only.

## Data preparation
The dataset is recorded in a controlled environment with professional recording tools, then processed by our home-build tool for annotation.
The annotation process includes:
- Transcription: the text is transcribed by a professional transcriber.
- Alignment: the text is aligned with the audio by a professional aligner.
- Elimination: the bad audio part is removed by an user to make the dataset clean.

## Data format
The dataset is organized in the following structure:
```bash
├── data
│   ├── wav
│   │   ├── 000001.wav
│   │   ├── 000002.wav
│   │   ├── 000003.wav
........
│   ├── metadata.csv
```

The metadata.json file contains the following information:
```bash
{
    "000001": {
        "text": "Hôm nay là thứ hai",
        "audio": "wav/000001.wav",
        "n_tokens": 5,
        "duration": 2.0
    },
    "000002": {
        "text": "Hôm nay là thứ ba",
        "audio": "wav/000002.wav",
        "n_tokens": 5,
        "duration": 2.0
    },
    ...
}
```

## Data statistics table
| Dataset |  text | audio | duration |  n_tokens |
| ------- |-----------|-------|------------|--------|
| count   | 10233     | 10233 | 10233      | 10233  |
| mean    | -         | -     | 3.634935   | 16.557412 |
| std     | -         | -     | 2.164213   | 9.852908 |
| min     | -         | -     | 0.128027   | 1.0    |
| 25%     | -         | -     | 1.920000   | 9.0    |
| 50%     | -         | -     | 3.168027   | 15.0   |
| 75%     | -         | -     | 4.960000   | 22.0   |
| max     | -         | -     | 18.210000  | 74.0   |
|sum      | -         | -     | 37196.2859 | 169432 |

## Samples
Here are some samples from the dataset:
- [10000.wav](https://drive.google.com/file/d/1w60td0FO5AnC88cc0maUydnsw5q3zWL0/view?usp=share_link)
- [10001.wav](https://drive.google.com/file/d/1w60td0FO5AnC88cc0maUydnsw5q3zWL0/view?usp=share_link)

## Application
- To prove that this dataset is useful for TTS application, we have trained a TTS model using this dataset and create an app (baonoi.ai) using this model.
- Sample generated audio: [g01.wav](https://drive.google.com/file/d/1CcyHCXoS5m9ILgBsWY-RZY52JNaZjjge/view?usp=share_link)
