# Semantic Segmentation of Panoramic Images (ADE20K, PyTorch)

This repository provides a **Google Colab–ready workflow** for **semantic segmentation of panoramic images** using a **pretrained ADE20K model** from the MIT CSAIL `semantic-segmentation-pytorch` framework.  
The pipeline generates **color-coded segmentation images** and **CSV files with pixel counts per semantic class**, suitable for urban environment and streetscape analysis.

---

## Model
- Framework: PyTorch  
- Encoder: ResNet50 Dilated  
- Decoder: Pyramid Pooling Module (PPM)  
- Dataset: ADE20K (150 semantic classes)  
- Source: MIT CSAIL Semantic Segmentation

---

## Requirements
- Google Colab (GPU recommended)
- Google Drive
- Python 3.x

All dependencies and pretrained model weights are downloaded automatically in Colab.

---


---

## Usage (Google Colab)

1. **Open the notebook in Google Colab**  
   Enable GPU: `Runtime → Change runtime type → GPU`

2. **Run the setup cell**  
   Installs dependencies, clones the MIT CSAIL repository, and downloads pretrained ADE20K weights (run once per session).

3. **Mount Google Drive**  
   Used for reading input images and saving outputs.

4. **Set input/output paths**  
   Paths are defined using Colab form parameters (`@param`) for interactive configuration.

5. **Run segmentation**  
   The pipeline loads images, performs semantic segmentation, aggregates pixel counts by observation point, and saves outputs.

---

## Outputs
- **Segmented images**  
  `segmented_<original_filename>.jpg` (original image + color-coded semantic map)

- **CSV file**  
  Pixel counts per ADE20K semantic class, aggregated by observation point.

---

## Notes
- Semantic (scene-level) segmentation, not instance segmentation  
- Consistent filename structure is required for correct aggregation  
- GPU significantly improves performance for large images

---

## Citation
If used in academic work, please cite:  
Zhou et al. (2018). *Semantic Understanding of Scenes through the ADE20K Dataset*. IJCV.  
MIT CSAIL Semantic Segmentation PyTorch Repository.

---

## License
This project follows the license of the original MIT CSAIL `semantic-segmentation-pytorch` repository.
