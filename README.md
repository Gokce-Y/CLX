# Waste Classification Using Computer Vision

This project compares different computer vision approaches for waste image classification using the TrashNet dataset.

The goal is to classify waste images into six categories:

* cardboard
* glass
* metal
* paper
* plastic
* trash

The project includes exploratory data analysis, data augmentation, CNN training, transfer learning, YOLOv8n training, and evaluation of a pre-trained MobileNetV2 model.

## Environment

This project was originally developed using a local virtual environment called:

```text
venv311
```

This is an older project environment that was used during development. If the notebooks run without errors, `venv311` can be used.

However, if dependency or package version errors occur, it is also possible to create and use a new virtual environment.

Example:

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

Activate it on macOS/Linux:

```bash
source venv/bin/activate
```

## Recommended Execution Order

Run the notebooks in the following order:

```text
1. 0_EDA.ipynb
2. 1_augmentation.ipynb
3. 2_cnn_transfer_learning_model_comparison.ipynb
4. 3_compare_yolo_cnn_splits.ipynb
5. 4_yolo_training_clean_split.ipynb
6. 5_huggingface_pretrained_mobilenet_evaluation.ipynb
```

## Important Notes

* The augmented dataset is only used for training.
* Validation and test sets are kept unchanged.
* The YOLO experiment uses full-image bounding boxes because real bounding box annotations are not available.
* The Hugging Face / pre-trained MobileNetV2 model is used as an external benchmark and should be interpreted separately from the models trained in this project.
