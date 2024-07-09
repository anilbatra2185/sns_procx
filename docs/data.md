<div align="center">

<h2><a href="https://arxiv.org/abs/2311.15964"><image src="./assets/eccv.png" alt="ECCV 2024" width=5%/> Efficient Pre-training for Localized Instruction Generation of Videos</a></h2>

[Anil Batra](https://anilbatra2185.github.io/), [Davide Moltisanti](https://www.davidemoltisanti.com/research/), [Laura Sevilla-Lara](https://laurasevilla.me/), [Marcus Rohrbach](https://rohrbach.vision/), [Frank Keller](https://homepages.inf.ed.ac.uk/keller/)

</div>

<h5 align="center">

[![arXiv](https://img.shields.io/badge/Arxiv-2311.15964-AD1C18.svg?logo=arXiv)](https://arxiv.org/abs/2311.15964)
[![Dataset](https://img.shields.io/badge/%F0%9F%A4%97%20Dataset-Sieve%20%26%20Swap-blue)](https://huggingface.co/datasets/anilbatra/sieve_and_swap)  <br>

</h5>

## Dataset Details - :hugs: [Hugging Face](https://huggingface.co/datasets/anilbatra/sieve_and_swap)

### Commands to download
Install :hugs: Huggingface Hub Library using the following command
```
conda install -c conda-forge huggingface_hub
```

Download the full dataset from the hub using the following command:

```
huggingface-cli download --repo-type dataset anilbatra/sieve_and_swap --local-dir ./
```

### Directory Structure
```
root
│
└───downstream ## instructional videos annotations utilized for training/finetuning the models
│   └───yc2
│       └───features.tar.gz ## S3D features for all the videos
│       └───data
│           └─── yc2_duration_frame.csv
│           └─── captiondata
│              └─── yc2_train.json
│              └─── yc2_val_official_available.json
│   └───tasty
│       └───features.tar.gz ## S3D features for all the videos
│       └───data
│           └─── yc2_duration_frame.csv
│           └─── captiondata
│               └─── ..
│
└───pretraining
│       └───features
│          └───features.tar.gz ## S3D features for all the videos
│       └───data
│           └─── htmrkb_dis_train_48k_6july_yc2format_clean.json
│           └─── htmrkb_dis_valid_3k_6july_yc2format_clean.json
│           └─── htmrkb_dis_train_48k_6july_yc2format_raw_transcript.json
│           └─── htmrkb_dis_valid_3k_6july_yc2format_raw_transcript.json
|
└───tokenizer ## Huggingface transformer based tokenizer files
│       └─── tokenizer.json
│       └─── special_tokens_map.json
│       └─── tokenizer_config.json
|
└───raw_data
│       └─── htm100_recipeNLG_mapping_iou_0_dot_1_recall_0_dot_3.json
│       └─── whisper_transcription.tar.gz ## video transcripts obtained from Whisper Model
│       └─── timed_transcripts.tar.gz ## Formatted with <start> ASR Text <end>
│       └─── howto100mDB ## filtered videos raw data
│       └─── recipeDB ## recipe instructions and embeddings
|
```


### Example Json Data

*YC2 Sample Data*
```
{
    "xHr8X2Wpmno": {
        "duration": 206.86,
        "timestamps": [
            [
                47,
                60
            ],
            [
                67,
                89
            ],
            [
                91,
                98
            ],
            ..
        ],
        "sentences": [
            "pick the ends off the verdalago",
            "combine lemon juice sumac garlic salt and oil in a bowl",
            "chop lettuce and place it in a bowl",
            ..
        ]
    },
    ..
}
```

*Pre-Training Sample Data*
```
{
    "bCvyCFkIU9k": {
        "duration": 571,
        "timestamps": [
            [
                11.48,
                34.72
            ],
            [
                39.24,
                52.2
            ],
            [
                52.2,
                64.24000000000001
            ],
            ..
        ],
        "sentences": [
            [
                "make rye dough by adding 2 tablespoons molasses , caraway seed , cocoa powder and 1 1 / 4 cups rye flour to 1 / 3 of batter",
                "to make the light rye , stir together the flours , salt , yeast , and caraway seeds in a 4 - quart bowl "
            ],
            [
                "add all flour and 1 1 / 4 cups bread flour blend well",
                "stir in 1 cup bread flour and mix until blended"
            ],
            [
                "notes this is a very easy and forgiving recipe",
                "this recipe is very forgiving of time and temperature"
            ],
            ..
        ]
    },
    ..
}
```