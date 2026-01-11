# CNN-Based Music Instrument Recognition System

<div align="center">
  <img src="https://raw.githubusercontent.com/yourusername/yourrepo/main/assets/mel_spectrograms.png" width="600" alt="Mel Spectrograms">
  <p><em>Multi-resolution Mel Spectrogram Analysis of Different Instruments</em></p>
</div>

## 📌 Overview
A deep learning system for recognizing 11 musical instruments from audio signals using optimized multi-resolution CNN architecture with enhanced regularization and data augmentation.

### Key Features
- 🎛 Multi-resolution Mel spectrogram analysis (64/96/128 bands)
- 🔊 Advanced audio augmentation pipeline (time/pitch shift, noise injection, filtering)
- 🧠 Hybrid CNN architecture with mixup regularization
- 📊 Comprehensive training monitoring and visualization
- 📦 Model versioning and production-ready export

## 🛠 Technologies
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.12%2B-orange)
![Librosa](https://img.shields.io/badge/Librosa-0.10%2B-yellowgreen)
![GPU](https://img.shields.io/badge/GPU-Accelerated-success)

## 📦 Installation
```bash
# Clone repository
git clone https://github.com/yourusername/instrument-recognition-system.git
cd instrument-recognition-system

# Install requirements
pip install -r requirements.txt

# Recommended requirements.txt
tensorflow==2.12.0
librosa==0.10.0
scikit-learn==1.2.2
numpy==1.24.3
matplotlib==3.7.1
seaborn==0.12.2
```

## ⚙️ Configuration
Modify `config.json` for different setups:
```json
{
  "sample_rate": 22050,
  "mel_bands": [64, 96, 128],
  "n_fft": 2048,
  "learning_rate": 0.0002,
  "max_files_per_instrument": 350,
  "augmentation_ratio": 0.85
}
```

## 🎵 Dataset Preparation
1. Download IRMAS-TrainingData from [MTG website](https://www.upf.edu/web/mtg/irmas)
2. Organize files:
```
IRMAS-TrainingData/
├── cel/        # Cello
├── cla/        # Clarinet
├── flu/        # Flute
... (11 instrument folders)
```

Supported instruments: `cello`, `clarinet`, `flute`, `acoustic_guitar`, `electric_guitar`, `organ`, `piano`, `saxophone`, `trumpet`, `violin`, `voice`

## 🚨 Troubleshooting
```markdown
### Common Issues
- **CUDA Out of Memory**: Reduce `batch_size` in training config
- **Protobuf Errors**: Set `PROTOCOL_BUFFERS_PYTHON_IMPLEMENTATION=python`
- **Dataset Path Errors**: Verify IRMAS folder structure matches requirements

### Performance Tips
- Enable GPU acceleration with CUDA 11.8+
- Use fast storage (SSD/NVMe) for audio processing
- Monitor memory usage with `nvidia-smi` (GPU) or `htop` (CPU)
```

## 📜 Citation
```bibtex
@misc{IRMASDataset,
  author = {Bosch, Juan J. and Marxer, Ricard and Gómez, Emilia},
  title = {Instrument Recognition in Musical Audio Signals},
  year = {2016},
  publisher = {MTG},
  url = {https://www.upf.edu/web/mtg/irmas}
}
```

## 📄 License
MIT License - See [LICENSE](LICENSE) for details
