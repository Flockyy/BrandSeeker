#  BrandSeeker

<div align="center">

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ACWrzkK7HLayllfno8cQ8iF9-1gYkx5g?usp=sharing)
[![Open in Kaggle](https://kaggle.com/static/images/open-in-kaggle.svg)](https://www.kaggle.com/code/humanbojack/brandseeker)
[![Python](https://img.shields.io/badge/Python-3.7+-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)](https://pytorch.org/)
[![YOLOv5](https://img.shields.io/badge/YOLOv5-00FFFF?style=flat-square)](https://github.com/ultralytics/yolov5)

**Automated brand detection in videos using YOLOv5 deep learning**

[Features](#-features)  [Installation](#-installation)  [Usage](#-usage)  [Dataset](#-dataset)  [Examples](#-examples)

</div>

---

##  Overview

BrandSeeker is a computer vision tool that automatically detects and tracks brand appearances in video content. Built on YOLOv5 architecture, it processes video frames to identify brand logos with configurable confidence thresholds and generates detailed analytics reports.

###  Key Features

- **38+ Brand Detection**: Recognizes major brands including tech, gaming, and consumer products
- **Video Processing**: Supports local files and YouTube URLs
- **Confidence Scoring**: Adjustable thresholds for detection accuracy
- **Frame Rate Control**: Customizable analysis frequency for performance optimization
- **PDF Reports**: Automated generation of brand appearance analytics
- **CLI Interface**: Simple command-line tool for batch processing

###  Supported Brands

<details>
<summary><b>Click to view all 38 detectable brands</b></summary>

- **Tech & Hardware**: Logitech, Corsair, Microsoft, DBrand, Rhinoshield
- **Gaming**: Republic of Gamers, World of Tanks, Raid Shadow Legends, War Thunder, Genshin Impact, State of Survival
- **Streaming & Entertainment**: Crunchyroll, Redbull, Fruitz
- **Services**: ExpressVPN, NordVPN, TunnelBear VPN, Surfshark, Honey Coupon, SkillShare, Brilliant.org
- **E-commerce**: Amazon, Audible, Lootcrate, Ridge Wallet
- **Food & Beverage**: Hello Fresh, Dollar Shave Club, Coca Cola, Uber Eats, GFuel, Gorillas
- **Other**: Displate, KiwiCo, Manscaped, Squarespace, Winamax

</details>

---

##  Installation

### Prerequisites

- Python 3.7 or higher
- PyTorch (with CUDA support recommended for GPU acceleration)

### Setup

```bash
# Clone the repository
git clone https://github.com/Flockyy/BrandSeeker.git
cd BrandSeeker/App

# Install dependencies
pip install -r requirements.txt
```

---

##  Usage

### Quick Start

```bash
# Place your video in the input_video folder
# Run detection with default settings
python brandseeker.py
```

### Advanced Configuration

```bash
# Analyze a YouTube video
python brandseeker.py --url "https://www.youtube.com/watch?v=VIDEO_ID"

# Custom framerate for faster processing
python brandseeker.py --framerate 10

# Adjust confidence weighting
python brandseeker.py --alpha 0.7

# Save raw detection data
python brandseeker.py --save-unprocessed-output
```

### Command-Line Options

| Option | Description | Default |
|--------|-------------|---------|
| `-U, --url` | Video URL (YouTube or direct link) | None |
| `-F, --framerate` | Analysis frame rate | 15 |
| `-S, --source` | Input video directory | `./input_video` |
| `-O, --save-dir` | Output directory for reports | `./predictions` |
| `-A, --alpha` | Confidence weight [0-1] | None |
| `--save-unprocessed-output` | Export raw detection data | False |

---

##  Output

Detection results are saved in the `predictions` folder as PDF reports containing:
- Brand appearance timeline
- Confidence scores for each detection
- Frame-by-frame analysis
- Summary statistics

---

##  Dataset

This project uses a custom-trained YOLOv5 model with a brand detection dataset available on [Kaggle](https://www.kaggle.com/datasets/humanbojack/yolo-brand-object-detection).

**Dataset Features:**
- 38 brand categories
- Thousands of annotated frames
- Real-world video content scenarios
- YOLO format annotations

---

##  Technology Stack

- **YOLOv5**: State-of-the-art object detection framework
- **PyTorch**: Deep learning backend
- **OpenCV**: Video processing and frame extraction
- **Python 3.7+**: Core implementation language

---

##  Examples

### Example 1: YouTube Video Analysis
```bash
python brandseeker.py --url "https://www.youtube.com/watch?v=dQw4w9WgXcQ" --framerate 20
```

### Example 2: High-Confidence Detection
```bash
python brandseeker.py --alpha 0.9 --framerate 30
```

---

##  Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Add new brand categories

---

##  License

This project is built upon [YOLOv5](https://github.com/ultralytics/yolov5) by Ultralytics.

---

##  Acknowledgments

- **YOLOv5** by Ultralytics for the detection framework
- **Kaggle Community** for dataset hosting and collaboration
- **Google Colab** for providing free GPU resources

---

<div align="center">

[ Back to Top](#-brandseeker)

</div>
