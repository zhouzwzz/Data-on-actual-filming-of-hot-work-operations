# Data on Actual Filming of Hot Work Operations

This repository provides metadata and access information for a public subset of an actual-filming hot work safety dataset.

The complete image and annotation subset is hosted on Hugging Face:

**Dataset link:** https://huggingface.co/datasets/ZhengwenZhou/Photos_hot_work

## Dataset Overview

The released dataset contains 600 randomly selected images and corresponding YOLO-format annotation files for computer-vision-based hot work safety monitoring.

The dataset was developed for object detection tasks related to unsafe conditions in hot work scenarios, including construction and industrial safety contexts. It is intended to support research on intelligent safety monitoring, occupational risk identification, and vision-based hazard recognition.

## Data Access

Due to file size considerations, the image and label files are not stored directly in this GitHub repository. Please download the dataset from Hugging Face:

https://huggingface.co/datasets/ZhengwenZhou/Photos_hot_work

This GitHub repository only stores:

- `sampled_600_manifest.csv`: list of the 600 selected image-label pairs
- `missing_labels.csv`: record of missing labels, if any
- `excluded_privacy_files.csv`: record of files excluded before sampling
- `README.md`: dataset description, citation information, and access instructions

## Dataset Structure on Hugging Face

The Hugging Face dataset contains the following structure:

```text
image/
labels/
sampled_600_manifest.csv
missing_labels.csv
excluded_privacy_files.csv
README.md
```

## Privacy and Access Limitations

This release is a partial public subset of a larger hot work safety dataset. Some original images contain privacy-sensitive information, including worker faces, identifiable personnel information, and hazardous-operation details. In addition, the full dataset cannot be released due to contractual and data-use restrictions.

Before random sampling, images with privacy-sensitive identifiers `00070-00073` and `00091-00094` were excluded.

Users should not attempt to identify workers, infer personal information, or use the dataset for purposes beyond occupational safety research.

## Annotation Format

The labels follow the YOLO annotation format:

```text
class_id x_center y_center width height
```

All coordinates are normalized to the range `[0, 1]`. Each annotation file corresponds to the image file with the same base filename.

## Citation

If you use this dataset or find it helpful for your research, please cite the following article:

Zhou, Z., Chen, S., Kou, J., Chen, S., Liu, J., & Guo, L. (2025). Integrating ontology and computer vision for intelligent monitoring of unsafe conditions in hot work. *Automation in Construction*, 180, 106574. https://doi.org/10.1016/j.autcon.2025.106574

## Acknowledgements

We sincerely thank the workers who participated in and supported the data collection process. Their contribution made this research possible. We also gratefully acknowledge the constructive comments and support from the reviewers and editors of the related publication.

We hope that this partial dataset can be used responsibly and effectively to support further research on intelligent construction safety, hot work risk monitoring, and human-centered occupational safety management.

## License and Use Restrictions

The dataset is released for academic research, algorithm testing, and non-commercial safety-related studies. Redistribution, commercial use, or attempts to recover private information are not permitted without explicit permission from the dataset owners.

## Repository Contents

```text
README.md
sampled_600_manifest.csv
missing_labels.csv
excluded_privacy_files.csv
```

The full image and annotation subset is available at:

https://huggingface.co/datasets/ZhengwenZhou/Photos_hot_work
