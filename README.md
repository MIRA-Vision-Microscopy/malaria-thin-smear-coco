# COCO-Formatted Bounding Box Annotations for the NIH Thin Blood Smear Malaria Dataset

This repository provides bounding box annotations in COCO format for the publicly available [NIH-NLM Thin Blood Smear Dataset](https://data.lhncbc.nlm.nih.gov/public/Malaria/NIH-NLM-ThinBloodSmearsPf/index.html) for *Plasmodium falciparum* detection. The annotations were generated through a combination of automated instance segmentation using Cellpose and targeted manual correction.

## Dataset Structure

The repository is organized as follows:
```bash
├── annotations/
│ ├── nih_polys_coco.json # COCO annotations for the polygon-labeled subset
│ ├── nih_points_coco.json # COCO annotations for the point-labeled subset (converted to boxes)
│ ├── categories.json # Class label definitions
├── README.md # Dataset documentation
├── LICENSE # Dataset license

```

- All annotation files follow the [COCO format](https://cocodataset.org/#format-data).
- Annotations include bounding boxes for three classes: non-infected red blood cells, infected red blood cells, and white blood cells.
- Each file corresponds to one of the original NIH subsets:
  - `nih_polys_coco.json`: derived from the 165 polygon-labeled images.
  - `nih_points_coco.json`: derived from the 800 point-annotated images.

## Modalities and Tasks

- **Modality**: Brightfield microscopy images of Giemsa-stained thin-blood smears.
- **Task**: Object detection of individual red and white blood cells, with classification into:
  - Non-infected red blood cells
  - Infected red blood cells
  - White blood cells

## Patient Information Fields

The annotation files do not include identifiable patient information. However, each image in the original NIH dataset is associated with one of 193 patients. The original dataset includes:
- 148 infected patients
- 45 uninfected patients
- 5 images per patient

Please refer to the original dataset publication for additional metadata:  
Kassim, Yasmin M., et al. *"Clustering-based dual deep learning architecture for detecting red blood cells in malaria diagnostic smears."* IEEE Journal of Biomedical and Health Informatics 25.5 (2020): 1735-1746.

[Link to dataset](https://lhncbc.nlm.nih.gov/publication/pub9932)

## Licensing and Usage

The original NIH dataset is provided under the following license terms:

- The data may be used, modified, and redistributed for commercial and non-commercial purposes.
- Attribution must be provided: “Courtesy of the U.S. National Library of Medicine.”
- Please cite the original dataset publication.

The annotation files in this repository are released under the same terms as the original dataset. If used, please cite the accompanying publication describing the annotation process and evaluation.

## Contact

For questions or feedback, please contact: [Frauke Wilm](mailto:fwilm@mira.vision)


