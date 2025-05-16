# Gender-Classification-4D
Gender Classification from DeepExplain-Derived fMRI Features

Research Question:

Do male and female brain activity show distinct patterns during face processing?



<img width="252" alt="image" src="https://github.com/user-attachments/assets/a9f80fdd-2fbb-4af8-b151-55cabe3f3c8f" />


Each color shows how important a voxel was for the CNN's face classification, So this data is attribution maps, not raw fMRI


<img width="145" alt="image" src="https://github.com/user-attachments/assets/7a18acfa-88ff-4bb2-8f6e-14371c6d70c2" />


4D data: (85×85×85×10) per subject

Load and reshape NIfTI data to 10×614125 per subject (timepoints × 85×85×85)
Normalize each time using z-score
Concatenated into a matrix: 850 × 614,125
PCA applied and 600 principal components retained for each subject 


<img width="403" alt="image" src="https://github.com/user-attachments/assets/d6ced543-3db0-4ebc-8368-7540cf92584f" />


850 samples (85 subjects × 10 timepoints)
Each sample has 614,125 voxels (from 85×85×85 volume)

After PCA: 850×614125 reduced to --> 850×600

Retained > 90% variance

<img width="232" alt="image" src="https://github.com/user-attachments/assets/fd6f4c94-e699-4034-a0d6-15e54dfa01ba" />



Applied logistic regression with LASSO regularization and used 5-fold cross-validation to select the optimal regularization parameter
Model trained to classify participant gender based on PCA-reduced fMRI features






# Model Performance:

<img width="329" alt="image" src="https://github.com/user-attachments/assets/3bd6059e-8053-4efa-a96c-665fe8eaa573" />


<img width="320" alt="image" src="https://github.com/user-attachments/assets/717a8b9d-b90e-41ad-951d-227d01da6f17" />


Result: The model was able to differentiate gender-related brain activity during face processing with approximately 90% accuracy


# Conclusion:

This project investigated gender differences in brain activity during face processing using CNN-based attribution maps. PCA and logistic regression revealed subtle distinctions between male and female neural patterns.


<img width="415" alt="image" src="https://github.com/user-attachments/assets/5d3a4ca0-59ab-4933-a9a0-1bf1265de232" />





