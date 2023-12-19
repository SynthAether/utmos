# UTMOS

This is an unofficial Python package for **UTMOS (UTokyo-SaruLab MOS Prediction System)**. This repository is based on the [original code](https://github.com/sarulab-speech/UTMOS22). The paper is available [here](https://arxiv.org/abs/2204.02152).

## What is UTMOS?

UTMOS is designed for calculating the mean opinion score (MOS) for a given voice sample. It can be used to calculate audio quality for datasets.

## Support

This implementation supports CPU, CUDA, and MPS, as well as ROCm if PyTorch is configured properly. This implementation will automatically use the GPU if available.

## Installation

```bash
pip install utmos
```

## Usage

### CLI (Command Line Interface)

```bash
utmos audio.wav
```

### Python API

```python
import utmos
model = Score() # The model will be automatically downloaded and will automatically utilize the GPU if available.
model.calculate_wav_file('audio_file.wav') # -> Float
# or model.calculate_wav(wav, sample_rate)
```

## License

This software is licensed under the MIT license.