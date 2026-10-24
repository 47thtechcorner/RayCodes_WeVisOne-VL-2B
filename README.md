<div align="center">
  <a href="https://youtu.be/xeCfugMN1d4">
    <img src="https://img.youtube.com/vi/xeCfugMN1d4/0.jpg" alt="Tencent's New 2B AI Replaces 6 Vision Models Of Apple, Qwen & Meta! (WeVisOne-VL Review)">
  </a>
  <h3>📺 <a href="https://youtu.be/xeCfugMN1d4">Watch the full video on YouTube</a></h3>
</div>

# WeVisOne-VL-2B: Unified Visual Perception Pipeline

[![License: Apache-2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Model Size: 2B](https://img.shields.io/badge/Model%20Size-2B%20%2B%209.6M%20Decoder-orange.svg)](https://huggingface.co/tencent/WeVisOne-VL-2B)
[![COCO Score](https://img.shields.io/badge/COCO%20Detection-85.8-brightgreen.svg)](https://huggingface.co/tencent/WeVisOne-VL-2B)
[![Local Footprint](https://img.shields.io/badge/Footprint-~1.6GB%20Q4%20%2F%204GB%20VRAM-purple.svg)](https://huggingface.co/mradermacher/WeVisOne-VL-2B-GGUF)

> *"A unified 2B vision-language model developed by WeChat Vision (Tencent) that handles object detection, spatial OCR, and soft edge cutouts in a single pass without chaining multiple separate models."*

---

### Pipeline Summary Matrix

| Practical Test | Input Image | Expected Output | Testing Objective |
| :--- | :--- | :--- | :--- |
| **01. Product Background Cutout** | Retail mug photo | Studio cutout with clean transparency | Preserve soft edges and fine steam |
| **02. Receipt Price & Tax Finder** | Dense store receipt scan | Color-highlighted price and tax boxes | Target exact numbers without confusion |
| **03. Missing Item Detector** | Dining table items | Visual verified-absent alert card | Confirm zero false alarms when missing |

---

## ⚡ Quick Start (Windows PowerShell)

Run the unified vision perception pipeline locally using Windows PowerShell:

### 1. Environment Setup
```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
pip install torch torchvision transformers pillow opencv-python numpy huggingface_hub
```

### 2. Download Official Model Weights
Download the official WeVisOne-VL-2B model weights and pixel decoder:
```powershell
hf download tencent/WeVisOne-VL-2B --local-dir models/WeVisOne-VL-2B
```

*Optional GGUF Quantization (for low VRAM / CPU):*
```powershell
hf download mradermacher/WeVisOne-VL-2B-GGUF WeVisOne-VL-2B.Q4_K_M.gguf --local-dir models/WeVisOne-VL-2B-GGUF
```

### 3. Run Production Pipeline
```powershell
python main.py
```

---

## 🎯 Practical Use Cases

- 🛍️ **Instant E-Commerce Product Studio**: Cut out products, cosmetics, and furniture with soft hair and glass edge transparency for catalogs.
- 🧾 **Receipt & Invoice Total Parsing**: Box exact tax lines, subtotals, and vendor stamps without confusing background text.
- 🛡️ **Missing Object Alerting**: Audit grocery shelves and security feeds with zero false positive boxes when items are gone.
- 🤖 **Robotic Pick-and-Place**: Deliver precise point coordinates (`<0>` to `<1000>`) directly to mechanical arms.

---

## 🗺️ Future Feature Roadmap

- ⚡ **Native GGUF & llama.cpp Stride-1 Execution**: C++ pixel decoder acceleration for resource-constrained setups.
- ✂️ **Real-Time Video Background Cutout**: Smooth webcam mask tracking for instant video calls.
- 🔍 **Interactive Click-to-Cut Canvas**: Browser-based click prompt to isolate objects instantly.
- 📱 **Mobile & WebAssembly Engine**: Run vision perception on-device via WebGPU.

---

## 🏷️ Search & Metadata Keywords

```text
WeVisOne,WeVisOne VL,WeVisOne 2B,Tencent AI,Qwen3 VL,Tencent vision AI,WeVisOne demo,Qwen visual AI,Qwen object detection,Qwen OCR,Meta SAM 2,Tencent vs Meta,vision language model,open source vision,local vision AI,2B vision model,Qwen3 VL tutorial,Tencent AI model,visual intelligence AI,Python vision model,multimodal AI model,local VLM,Qwen Vision,Local OCR,Vision Model,Tencent WeVisOne,WeVisOne VL 2B,Qwen3 VL 2B,Tencent Qwen,Qwen vision
```
