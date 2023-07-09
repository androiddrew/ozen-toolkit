# OZEN toolkit, AI powered audio dataset helper.
<a href='https://ko-fi.com/O4O5GU04F' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi2.png?v=3' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

OZEN is a small tool to help you process audio files to a LJ format.

Given a folder of files or a single audio file, it will extract the speech, transcribe using Whisper and save in the LJ format (wavs in wavs folder, train and valid txts).

## INSTALLATION

This Repo:

```bash
python3 -m venv env
source env/bin/activate
pip install pip-tools==6.14.0
pip-sync linux-py-3.10-requirements.txt linux-py-3.10-dev-requirements.txt
```


Upstream:
```sh
Accept the license terms on https://huggingface.co/pyannote/segmentation 
Install Anaconda or setup your own environment and install requirements
git clone https://github.com/devilismyfriend/ozen-toolkit
run Set Up Ozen.bat
```


## USAGE

Drag a folder or a file on the Drag_Here.bat to process it.

The first time you'll be prompted to provide an HuggingFace token, once you do a config file will be created where you can specifiy models to use, the validation/training data desired split and more.

Alternatively you can use ozen.py in cli.

### Orzen CLI

The first time you run the model you will end up creating a config file

```
python3 ozen.py <file_path>
```

You will be prompted for a HuggingFace token, a config.ini will be created for you, and models will be downloaded for transcription and diarization. After this initial setup the file path to your wav files will be used to transcibe and encode a new dataset that matches the LJ Speech format!
