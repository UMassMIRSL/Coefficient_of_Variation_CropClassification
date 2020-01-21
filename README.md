# Coefficient_of_Variation_CropClassification

This workflow uses a time series of SAR imagery to implement coefficient of variation (CV) for crop/non-crop classification using a Receiver Operating Characteristic (ROC) curve. The notebook statistically calculates the CV for a stack of time-series imagery. The CV output is then used to generate a ROC curve by using the USDA Cropland Data Layer (CDL) as ground truth. Pixels classified by the CDL as "Water" are masked and not used in classification because, water has a high variation measurement not comparable to the CV values of other non-cropland land covers and is often missclassified because of this. The statistic Youden's Index is calculated to detemine the ideal threshold on the curve to use for best classification results. The accuracy of the classification compared to the CDL as ground truth are calculated for the CV crop/non-crop classification. The classified image is exported as a Geotiff. A CSV file is exported containing accuracy statistics for the classification.

Coefficient of Variation is calculated by: Standard Deviation/Mean

Created by: Shannon Rose, Microwave Remote Sensing Labratory (MIRSL) Unuversity of Massachusetts- Amherst

Datasets needed:

    Timeseries of SAR imagery
    
    CDL available at https://nassgeodata.gmu.edu/CropScape/
    
This code was written and best used within Jupyter Notebook, but can be used anywhere python code can be run. 
