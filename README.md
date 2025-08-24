# Corn_Field_Classification_Python_Project

Sentinel-2 Corn Field Classification Project
Project Overview

This project analyzes satellite imagery from Sentinel-2 to classify corn fields in Iowa using wavelength analysis. By examining different spectral layers (True Color, EVI, Barren Soil, Agriculture, and a custom layer), the system identifies the characteristic wavelengths of corn plants and maps them across agricultural areas.

Methodology

1. Data Collection

  Collected Sentinel-2 satellite imagery of Iowa corn fields
  
  Focused on multiple spectral layers:
  
    True Color (natural color representation)
    
    EVI (Enhanced Vegetation Index)
    
    Barren Soil
    
    Agriculture
    
    Custom layer (B03, B08, B05 bands) optimized for corn detection

2. Wavelength Analysis

  Developed an algorithm to convert RGB pixel values to approximate wavelengths (380-750 nm)
  
  For each image layer, calculated statistical properties of wavelengths:
  
    Mean, median, and mode wavelengths
    
    Standard deviation
    
    Minimum and maximum values    
    
    Frequency distribution of wavelengths

3. Corn Signature Identification

  Analyzed fields with at least 80% corn coverage
  
  Identified the top 10 most frequent wavelengths as the "corn signature"
  
  These characteristic wavelengths serve as fingerprints for corn plants

4. Classification Algorithm

  Developed a pixel-matching algorithm to detect corn presence
  
  Highlights pixels matching the corn signature wavelengths (within tolerance)
  
  Counts and visualizes corn pixels across different layers

Key Findings

  Custom layer provided the best classification results (~90% accuracy)
  
  Each layer revealed different spectral characteristics of corn fields
  
  The custom layer (B03, B08, B05) proved most effective for corn detection
  
  Wavelength analysis successfully distinguished corn from other vegetation and soil

Technical Implementation

Core Functions

1. RGB to Wavelength Conversion:

  Converts RGB values to approximate wavelengths using hue calculation
  
  Maps hue values (0-360°) to visible spectrum wavelengths (380-750 nm)

2. Image Analysis:
  
  Processes satellite images to extract wavelength information
  
  Calculates statistical properties of wavelength distributions
  
  Identifies dominant wavelengths (modes) in corn fields

3. Classification Visualization:

  Highlights pixels matching target wavelengths
  
  Generates comparative visualizations of original and classified images
  
  Provides quantitative analysis of corn coverage

Usage

The project processes Sentinel-2 imagery through wavelength analysis and classification:

  1. Load satellite images from different spectral layers
  
  2. Convert pixel values to wavelength approximations
  
  3. Analyze wavelength distributions to identify corn signatures
  
  4. Apply classification to detect corn pixels in new imagery
  
  5. Visualize results with statistical reports and highlighted images

Requirements

  Python 3.7+
  
  NumPy
  
  OpenCV
  
  scikit-image
  
  Matplotlib
  
  Pillow
  
  SciPy

Applications

This methodology can be adapted for:

  Precision agriculture monitoring
  
  Crop type classification
  
  Vegetation health assessment
  
  Land use mapping
  
  Environmental monitoring

The project demonstrates the effectiveness of wavelength analysis for agricultural classification using satellite imagery, with particular success in identifying corn fields based on their spectral signatures.


