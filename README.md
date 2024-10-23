# README

## Project Introduction

This project focuses on cell clustering based on coordinates from each frame extracted from a pretrained GNN model in [Graph Neural Network for Cell Tracking in Microscopy Videos (ECCV 2022)](https://github.com/talbenha/cell-tracker-gnn/tree/main). The dataset used is the **Fluo_C2DL_Huh7** from the Cell Tracking Challenge.
## Dataset

The dataset consists of 30 frames and contains 37 cells. It provides rich information for tracking and analyzing cell movements over time. Below are demo images and a video of the dataset:

![Dataset Image](https://github.com/quang2719/Cell-Tracking-using-GNN/blob/main/demo_image/original_data.png)  
[Demo Video](https://github.com/quang2719/Cell-Tracking-using-GNN/blob/main/demo_image/Demo_cell_video_v1.mp4)
### Process Overview

1. **Handling Missing Data**: Cells that are absent in some frames are processed using Forward Fill and Backward Fill methods.

2. **Data Preprocessing**: The data is transformed into a tabular format suitable for clustering.

3. **Data Visualization**: Cells and their paths in the 2D space are visualized as follows:  
   ![Visualization Image](https://github.com/quang2719/Cell-Tracking-using-GNN/blob/main/demo_image/cell_visual.png)

4. **Cell Clustering**: Cells are clustered based on their paths using the K-means algorithm with various k values as shown below:  
   ![Image k=1](https://github.com/quang2719/Cell-Tracking-using-GNN/blob/main/demo_image/Screenshot%202024-10-23%20130444.png)  
   ![Image k=2](https://github.com/quang2719/Cell-Tracking-using-GNN/blob/main/demo_image/Screenshot%202024-10-23%20130453.png)  
   ![Image k=3](https://github.com/quang2719/Cell-Tracking-using-GNN/blob/main/demo_image/Screenshot%202024-10-23%20130501.png)  
   ![Image k=4](https://github.com/quang2719/Cell-Tracking-using-GNN/blob/main/demo_image/Screenshot%202024-10-23%20130509.png)  
   ![Image k=5](https://github.com/quang2719/Cell-Tracking-using-GNN/blob/main/demo_image/Screenshot%202024-10-23%20130516.png)  
   ![Image k=6](https://github.com/quang2719/Cell-Tracking-using-GNN/blob/main/demo_image/Screenshot%202024-10-23%20130523.png)  
   ![Image k=7](https://github.com/quang2719/Cell-Tracking-using-GNN/blob/main/demo_image/Screenshot%202024-10-23%20130530.png)  
   ![Image k=8](https://github.com/quang2719/Cell-Tracking-using-GNN/blob/main/demo_image/Screenshot%202024-10-23%20130530.png)  

5. **Choosing the Optimal k**: The Elbow method is used to determine that k = 4 is the most suitable value. Below is the elbow chart:  
   ![Elbow Chart](https://github.com/quang2719/Cell-Tracking-using-GNN/blob/main/demo_image/Elbow.png)  
   ![Image k=4](https://github.com/quang2719/Cell-Tracking-using-GNN/blob/main/demo_image/k_4.png)

## Conclusion

The project successfully clustered cells based on coordinates, providing valuable insights into cell behavior and movement in a 2D environment.
