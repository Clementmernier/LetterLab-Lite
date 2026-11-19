# LetterLab Lite

**LetterLab Lite** is an image dataset designed for Optical Character Recognition (OCR) tasks, particularly handwritten or printed uppercase letter recognition.

## Dataset Overview

The dataset contains **48,000 images** distributed across 24 classes, with 2,000 images per class.

| Property | Description |
|---|---|
| Total images | ≈48,000 |
| Number of classes | 24 |
| Images per class | ≈2,000 |
| Classes | Uppercase letters (A–Z, excluding 2 letters) |
| Format | PNG |
| Naming convention | `LETTER_XXXXX.png` |
| License | CC BY-SA 4.0 |

## Repository Structure

```text
LetterLab-Lite/
├── CITATION.cff
├── dataset/
│   └── LetterLab-Lite.tar.gz
├── LICENCE
└── README.md
```

The dataset is distributed as a compressed TAR archive (`.tar.gz`) to simplify downloading and storage.


Once extracted, the dataset follows this structure:

```text
dataset/
├── A/
│   ├── A_00001.png
│   ├── A_00002.png
│   └── ...
├── B/
│   └── ...
├── C/
│   └── ...
...
└── Z/
    └── ...
```

Each class has its own directory, named after the corresponding uppercase letter.

Image filenames follow the convention:

`LETTER_XXXXX.png`

Where:
- `LETTER` is the corresponding uppercase letter.
- `XXXXX` is a five-digit identifier.

## Download and Extraction

The dataset archive is located in the `dataset/` directory.

Extract it from the repository root using:

```bash
tar -xzf dataset/LetterLab-Lite.tar.gz
```

To inspect its contents without extracting:

```bash
tar -tzf dataset/LetterLab-Lite.tar.gz
```


## Usage

The directory structure is compatible with common machine learning workflows.

For example, using Python:

```python
from pathlib import Path

dataset_path = Path("dataset")

for class_dir in sorted(dataset_path.iterdir()):
    if class_dir.is_dir():
        images = list(class_dir.glob("*.png"))
        print(f"{class_dir.name}: {len(images)} images")
```

This organization makes it straightforward to load images by class and prepare training, validation and testing datasets.

## License

LetterLab Lite is distributed under the **Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)** license.

You are free to:
- Share — copy and redistribute the material.
- Adapt — remix, transform and build upon the material.

Under the following terms:
- **Attribution:** You must give appropriate credit to the original dataset.
- **ShareAlike:** If you modify or build upon the dataset, you must distribute your contributions under the same license.

Please refer to the [LICENSE](LICENSE) file for the complete license terms.

### Attribution

If you use this dataset in a project, publication or research work, please provide attribution.

Suggested attribution:

> LetterLab Lite — [Author], [Year]. Source: [Repository URL]. License: CC BY-SA 4.0. Modifications: None.

If you modify the dataset, please indicate the changes made.

## Citation

A `CITATION.cff` file is provided to facilitate proper citation of this dataset.

GitHub can automatically generate citation information from this file using the **"Cite this repository"** feature.

## Contributing

Contributions, improvements and feedback are welcome.

If you find an issue with the dataset or have suggestions for improvements, feel free to open an issue or submit a pull request.

---

**LetterLab Lite** — A lightweight dataset for uppercase letter recognition.
