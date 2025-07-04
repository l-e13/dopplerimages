# Project 3- Doppler Images

## Goal
Detect the alphabetical and numerical text from the velocity scale bar of aortic valve
Doppler images and return their pixel coordinates to calculate the pixel distance between them

## Software and Platform
### Types of Software Used: 
- Programming Language: Python
- Data Processing & Analysis:
  - pandas - Reading, cleaning, filtering, and merging the dataset
  - opencv - Image preprocessing steps such as grayscale conversion, histogram equalization, thresholding, cropping, and inversion
  - pytesseract - Performing OCR to extract text and spatial information from image regions
- Data Storage & Export: CSV Files
- Cloud Computing: Google Colab
### Packages Installed: 
  - pandas
  - matplotlib
  - opencv
  - pytesseract
  - numpy
  - csv
### Platforms Used: 
Windows & Mac

## Map of Documentation
```mermaid
graph TB
  A[dopplerimages]
  A1[README.md]
  A2[LICENSE.md]
  B[SCRIPTS]
  B1[EDA.ipynb]
  B2[Preprocessing.ipynb]
  B3[mass upload.ipynb]
  C[DATA]
  C1[ocr_results.csv]
  C2[Doppler_Images]
  C3[Data Appendix]
  D[OUTPUT]


  A --> A1
  A --> A2
  A --> B
  B --> B1
  B --> B2
  B --> B3
  A --> C
  C --> C1
  C --> C2
  C --> C3
  A --> D


  %% Styling for main project folder (Dark Blue)
  style A fill:#003366,stroke:#001f3f,stroke-width:2px,color:white;

  %% Styling for main categories (Light Blue)
  style A1 fill:#4a90e2,stroke:#003d5b,stroke-width:2px,color:white;
  style A2 fill:#4a90e2,stroke:#003d5b,stroke-width:2px,color:white;
  style B fill:#4a90e2,stroke:#003d5b,stroke-width:2px,color:white;
  style C fill:#4a90e2,stroke:#003d5b,stroke-width:2px,color:white;
  style D fill:#4a90e2,stroke:#003d5b,stroke-width:2px,color:white;

  %% Styling for subsets (Light Red)
  style B1 fill:#ff9999,stroke:#8b0000,stroke-width:1px,color:black;
  style B2 fill:#ff9999,stroke:#8b0000,stroke-width:1px,color:black;
  style B3 fill:#ff9999,stroke:#8b0000,stroke-width:1px,color:black;
  style C1 fill:#ff9999,stroke:#8b0000,stroke-width:1px,color:black;
  style C2 fill:#ff9999,stroke:#8b0000,stroke-width:1px,color:black;
  style C3 fill:#ff9999,stroke:#8b0000,stroke-width:1px,color:black;

```

## Reproduction Instructions

1. **Set up Environment**
    - install python
    - install required libraries (listed above)
  
2. **Download Dataset**
    - navigate to **DATA** folder
    - download `Doppler_Images` folder containing 40 images
    - store folder in Google Drive
      
3. **Text Extraction and Coordinates**
   - navigate to **SCRIPTS** folder
   - open `mass upload.ipynb`
   - run script to preprocess iamges, extract text, and get coordinates on each image
   - script will save text and coordinates in `ocr_results.csv`
  
4. **EDA**
   - navigate to **SCRIPTS** folder
   - open `EDA.ipynb`
   - upload `ocr_results.csv`
   - run script to produce EDA
     
5. **Analysis**
   - navigate to **SCRIPTS** folder
   - open `Analysis.ipynb`
   - upload `ocr_results.csv`
   - run script to produce `cm_m_300_distances.csv`, a file containing text sucessfully detected with units and the value 300 from the images
   - navigate to the file `Analysis Output.pdf` in the same folder to view a summary of the figures produced by the analysis
