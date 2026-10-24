# Football Object Detection Sample Dataset

This project shows the object detection annotation work of **Annomax AI** using football match images. It shows how we place bounding boxes, label objects the same way every time and check the quality of the final dataset for computer vision use.

## Project Overview

| Item | Details |
|------|---------|
| Project Name | Football Object Detection Sample Dataset |
| Organization | Annomax AI |
| Task Type | Image Annotation |
| Annotation Method | Bounding Box |
| Dataset Size | 20 images (planned) |
| Dataset Status | Portfolio Demonstration |

## Project Objectives

- Show accurate bounding box annotation of objects in football match images
- Find and label players and other football objects
- Keep the same annotation rules across all images
- Run quality checks to catch missed objects, wrong labels and loose bounding boxes
- Prepare clean annotations for object detection and sports analytics work

## Object Classes

| Class ID | Class Name | Description |
|----------|------------|-------------|
| 0 | player | Outfield football players |
| 1 | goalkeeper | Players acting as goalkeepers |
| 2 | referee | Match officials visible on the pitch |
| 3 | ball | The football used during the match |
| 4 | goalpost | Visible goal frames and posts |

Class IDs are only for documentation and keeping labels consistent. The final exported IDs must follow the class setup of the annotation platform.

## Annotation Guidelines

- Give every visible target object its own bounding box, even when many players are close together or overlap
- Overlapping bounding boxes are fine when objects are close or when one blocks part of another
- Draw each box as tight as possible around the visible edges of the object and try not to include parts of nearby objects
- Never merge many players into one bounding box
- When one player partly blocks another, annotate the visible part of each player following the project guidelines
- If an object is heavily blocked and its edges are hard to see, annotate the clear visible part and flag it for review if needed

## Dataset Structure

This is the recommended folder structure:

```
football-object-detection-dataset/
├── README.md
├── classes.txt
├── images/
│   ├── image_001.jpg
│   ├── image_002.jpg
│   └── ...
├── annotations/
│   └── annotations.json
├── preview/
│   └── annotated_samples/
└── qa_report.xlsx
```

The real folder structure can be different depending on the annotation platform and export format.

## Annotation Format

The dataset can be exported in COCO JSON or YOLO format depending on what the project needs.

- **COCO JSON:** keeps image info, category definitions and bounding box coordinates in one structured JSON file
- **YOLO:** keeps class IDs and normalized bounding box coordinates in text files, usually one label file for each image

Before finishing, the final export should be checked so that class IDs, image references and bounding box coordinates are all correct.

## Quality Assurance

The dataset is reviewed for:

- Correct object class
- Accurate bounding box placement
- Missing visible objects
- Duplicate annotations
- Wrong or inconsistent labels
- Too much background inside bounding boxes
- Invalid or incomplete annotation records
- Consistent image and label file names
- Correct export structure and coordinate values

A second review should be done before finalizing the dataset whenever possible.

## Potential Applications

This type of annotated data can help with:

- Football player detection
- Sports object tracking
- Player counting and positioning
- Football match analysis
- Sports video analytics
- Computer vision model development
- Automated sports content analysis

This sample only shows annotation methods. It does not claim that a trained or validated AI model has been built.

## Data Source and Usage

Images should come from original sources that allow the planned use. Source info and license details should be written down where available.

This dataset is made for portfolio demonstration and service evaluation. It is not client work and it is not production ready training data.

Sharing the source images and annotations again must follow the image licenses and permissions.

## About Annomax AI

Annomax AI offers AI data annotation, data processing and quality assurance services for businesses and AI development teams.

- **Website:** [www.annomaxai.com](https://www.annomaxai.com)
- **Email:** sales@annomaxai.com

## Disclaimer

This is a portfolio demonstration project made to show image annotation workflows, labeling consistency and quality assurance practices. Real dataset performance and fit depend on the needs of each project.

---

*Note: This is a sample dataset for demonstration purposes. Please verify the image usage rights and licensing before redistributing the images or using them commercially.*
