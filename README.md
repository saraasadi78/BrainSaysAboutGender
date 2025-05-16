# Gender-Classification-4D
Gender Classification from DeepExplain-Derived fMRI Features

Research Question:

Do male and female brain activity show distinct patterns during face processing?



<img width="252" alt="image" src="https://github.com/user-attachments/assets/a9f80fdd-2fbb-4af8-b151-55cabe3f3c8f" />


Each color shows how important a voxel was for the CNN's face classification, So this data is attribution maps, not raw fMRI


<img width="145" alt="image" src="https://github.com/user-attachments/assets/7a18acfa-88ff-4bb2-8f6e-14371c6d70c2" />


4D data: (85×85×85×10) per subject




<img width="403" alt="image" src="https://github.com/user-attachments/assets/d6ced543-3db0-4ebc-8368-7540cf92584f" />


850 samples (85 subjects × 10 timepoints). Each sample has 614,125 voxels (from 85×85×85 volume) After PCA: 850×614125 reduced to --> 850×600

Retained > 90% variance


