# <h1 align="center"><b> Ultimate RVC Maker 🎵 </b></h1>
<div align="center">



<div align="center">
  <img src="https://count.nett.moe/get/foo/img?theme=rule34" alt="yeh"></div>

</div>

<div align="center">
  
A high-quality voice conversion tool focused on ease of use and performance.

[![RVC MAKER](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/unchCrew/RVC-MAKER)
[![Open In Colab](https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252)](https://colab.research.google.com/github/TheNeodev/Notebook/blob/main/RVC-MAKER.ipynb)
[![Licence](https://img.shields.io/badge/LICENSE-MIT-green?style=for-the-badge)](https://github.com/UnchCrew/RVC-MAKER/blob/main/LICENSE)

[![Huggingface](https://img.shields.io/badge/🤗%20-Spaces-yellow.svg?style=for-the-badge)](https://huggingface.co/spaces/NeoPy/RVC-MAKER)


</div>

<div align="center">


</div>

# Description
This project is all in one, easy-to-use voice conversion tool. With the goal of creating high-quality and high-performance voice conversion products, the project allows users to change voices smoothly and naturally.


# ToDo Features

- Cli for colab notebook

# Project Features

| Feature | Description |
|---------|-------------|
| **Music Separation** | Utilizes MDX-Net for separating audio tracks. |
| **Voice Conversion** | Supports file conversion, batch conversion, conversion with Whisper, and text-to-speech conversion. |
| **Background Music Editing** | Enables editing and manipulation of background music tracks. |
| **Apply Effects to Audio** | Allows application of various effects to enhance or modify audio output. |
| **Generate Training Data** | Creates training data from linked paths for model training. |
| **Model Training** | Supports v1 and v2 models with high-quality encoders for training. |
| **Model Fusion** | Facilitates combining multiple models for enhanced performance. |
| **Read Model Information** | Provides functionality to access and display model metadata. |
| **Export Models to ONNX** | Enables exporting trained models to ONNX format for compatibility. |
| **Download from Pre-existing Model Repositories** | Allows downloading models from established repositories. |
| **Search for Models on the Web** | Supports searching for models online for easy access. |
| **Pitch Extraction** | Extracts pitch information from audio inputs. |
| **Support for Audio Conversion Inference Using ONNX Models** | Enables inference for audio conversion using ONNX-compatible models. |
| **ONNX RVC Models with Indexing** | Supports ONNX RVC models with indexing for efficient inference. |
| **Multiple Model Options** | |
| | **F0**: `pm, dio, mangio-crepe-tiny, mangio-crepe-small, mangio-crepe-medium, mangio-crepe-large, mangio-crepe-full, crepe-tiny, crepe-small, crepe-medium, crepe-large, crepe-full, fcpe, fcpe-legacy, rmvpe, rmvpe-legacy, harvest, yin, pyin, swipe` |
| | **F0_ONNX**: Some models converted to ONNX for accelerated pitch extraction. |
| | **F0_HYBRID**: Combines multiple options, e.g., `hybrid[rmvpe+harvest]`, or all options together. |
| | **EMBEDDERS**: `contentvec_base, hubert_base, japanese_hubert_base, korean_hubert_base, chinese_hubert_base, portuguese_hubert_base` |
| | **EMBEDDERS_ONNX**: Pre-converted ONNX versions of embedding models for accelerated extraction. |
| | **EMBEDDERS_TRANSFORMERS**: Pre-converted Hugging Face versions of embedding models as an alternative to Fairseq. |
| | **SPIN_EMBEDDERS**: A new embedding extraction model offering potentially higher quality than older methods. |

___

# Installation and Usage

- **Step 1**: Install Python from the official website or [Python](https://www.python.org/ftp/python/3.10.7/python-3.10.7-amd64.exe) (**REQUIRES PYTHON 3.10.x OR PYTHON 3.11.x**)
- **Step 2**: Install FFmpeg from [FFMPEG](https://github.com/BtbN/FFmpeg-Builds/releases), extract it, and add it to PATH
- **Step 3**: Download and extract the source code
- **Step 4**: Navigate to the source code directory and open Command Prompt or Terminal
- **Step 5**: Run the command to install the required libraries
  
```
python -m venv envenv\Scripts\activate
```

If you have an NVIDIA GPU, run this step depending on your CUDA version (you may need to change cu117 to cu128, etc.):

If using Torch 2.3.1
```
python -m pip install torch==2.3.1 torchaudio==2.3.1 torchvision==0.18.1 --index-url https://download.pytorch.org/whl/cu117
```

If using Torch 2.6.0
```
python -m pip install torch==2.6.0 torchaudio==2.6.0 torchvision==0.21.0 --index-url https://download.pytorch.org/whl/cu117
```

Then run:
```
python -m pip install -r requirements.txt
```

- **Step 6**: Run the `run_app` file to open the user interface (Note: Do not close the Command Prompt or Terminal for the interface)
- Alternatively, use Command Prompt or Terminal in the source code directory
- To allow the interface to access files outside the project, add `--allow_all_disk` to the command:

```
env\Scripts\python.exe main\app\app.py --open
```

**To use TensorBoard for training monitoring**:

Run the file: tensorboard or the command

```
env\Scripts\python.exe main\app\tensorboard.py
```

# Command-Line Usage

```
python main\app\parser.py --help

```


# NOTES

- **This project only supports NVIDIA GPUs**
- **Currently, new encoders like MRF HIFIGAN do not yet have complete pre-trained datasets**
- **MRF HIFIGAN and REFINEGAN encoders do not support training without pitch training**
- **Models in the URVC repository are collected from AI Hub, HuggingFace, and other repositories. They may carry different licenses (For example, Audioldm2 has model weights with a "Non-Commercial" clause).**
- **This source code contains third party software components licensed under "non-commercial" terms. Any commercial use, including solicitation of donations or financialization of derivatives, may violate the license and will be subject to appropriate legal liability.**

# Terms of Use

- You must ensure that the audio content you upload and convert through this project does not violate the intellectual property rights of third parties.

- The project must not be used for any illegal activities, including but not limited to fraud, harassment, or causing harm to others.

- You are solely responsible for any damages arising from improper use of the product.

- I will not be responsible for any direct or indirect damages arising from the use of this project.

# This Project is Built Based on the Following Projects



| Project | Author/Organization | License |
|---------|---------------------|---------|
| [Vietnamese-RVC](https://github.com/PhamHuynhAnh16/Vietnamese-RVC) | Phạm Huỳnh Anh | MIT License |
| [Applio](https://github.com/IAHispano/Applio/tree/main) | IAHispano | MIT License |
| [Python-audio-separator](https://github.com/nomadkaraoke/python-audio-separator/tree/main) | Nomad Karaoke | MIT License |
| [Retrieval-based-Voice-Conversion-WebUI](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI/tree/main) | RVC Project | MIT License |
| [RVC-ONNX-INFER-BY-Anh](https://github.com/PhamHuynhAnh16/RVC_Onnx_Infer) | Phạm Huỳnh Anh | MIT License |
| [Torch-Onnx-Crepe-By-Anh](https://github.com/PhamHuynhAnh16/TORCH-ONNX-CREPE) | Phạm Huỳnh Anh | MIT License |
| [Hubert-No-Fairseq](https://github.com/PhamHuynhAnh16/hubert-no-fairseq) | Phạm Huỳnh Anh | MIT License |
| [Local-attention](https://github.com/lucidrains/local-attention) | Phil Wang | MIT License |
| [TorchFcpe](https://github.com/CNChTu/FCPE/tree/main) | CN_ChiTu | MIT License |
| [FcpeONNX](https://github.com/deiteris/voice-changer/blob/master-custom/server/utils/fcpe_onnx.py) | Yury | MIT License |
| [ContentVec](https://github.com/auspicious3000/contentvec) | Kaizhi Qian | MIT License |
| [Mediafiredl](https://github.com/Gann4Life/mediafiredl) | Santiago Ariel Mansilla | MIT License |
| [Noisereduce](https://github.com/timsainb/noisereduce) | Tim Sainburg | MIT License |
| [World.py-By-Anh](https://github.com/PhamHuynhAnh16/world.py) | Phạm Huỳnh Anh | MIT License |
| [Mega.py](https://github.com/3v1n0/mega.py) | Marco Trevisan | No License |
| [Gdown](https://github.com/wkentaro/gdown) | Kentaro Wada | MIT License |
| [Whisper](https://github.com/openai/whisper) | OpenAI | MIT License |
| [PyannoteAudio](https://github.com/pyannote/pyannote-audio) | pyannote | MIT License |
| [AudioEditingCode](https://github.com/HilaManor/AudioEditingCode) | Hila Manor | MIT License |
| [StftPitchShift](https://github.com/jurihock/stftPitchShift) | Jürgen Hock | MIT License |
| [Codename-RVC-Fork-3](https://github.com/codename0og/codename-rvc-fork-3) | Codename;0 | MIT License |



# Model Repository for Model Search Tool

- **[VOICE-MODELS.COM](https://voice-models.com/)**

# Pitch Extraction Methods in RVC

This document provides detailed information on the pitch extraction methods used, including their advantages, limitations, strengths, and reliability based on personal experience.

| Method            | Type           | Advantages                | Limitations                  | Strength           | Reliability        |
|-------------------|----------------|---------------------------|------------------------------|--------------------|--------------------|
| pm                | Praat          | Fast                      | Less accurate                | Low                | Low                |
| dio               | PYWORLD        | Suitable for rap          | Less accurate at high frequencies | Medium             | Medium             |
| harvest           | PYWORLD        | More accurate than DIO    | Slower processing            | High               | Very high          |
| crepe             | Deep Learning  | High accuracy             | Requires GPU                 | Very high          | Very high          |
| mangio-crepe      | Crepe finetune | Optimized for RVC         | Sometimes less accurate than original crepe | Medium to high     | Medium to high     |
| fcpe              | Deep Learning  | Accurate, real-time       | Requires powerful GPU        | Good               | Medium             |
| fcpe-legacy       | Old            | Accurate, real-time       | Older                        | Good               | Medium             |
| rmvpe             | Deep Learning  | Effective for singing voices | Resource-intensive           | Very high          | Excellent          |
| rmvpe-legacy      | Old            | Supports older systems     | Older                        | High               | Good               |
| yin               | Librosa        | Simple, efficient         | Prone to octave errors       | Medium             | Low                |
| pyin              | Librosa        | More stable than YIN      | More complex computation     | Good               | Good               |
| swipe             | WORLD          | High accuracy             | Sensitive to noise           | High               | Good               |

# Bug Reporting

- **If you encounter an error while using this source code, I sincerely apologize for the poor experience. You can report the bug using the methods below.**

- **you can report bugs to us via [ISSUE](https://github.com/unchCrew/RVC-MAKER/issues).**

