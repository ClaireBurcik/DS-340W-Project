# A Comparative Analysis of Clustering Algorithms for Marketing Customer Segmentation Applications

## About 
This project builds off of the research performed in the paper "An Exploration of Clustering Algorithms for Customer Segmentation in the UK Retail Market" (link: https://www.mdpi.com/2813-2203/2/4/42). The work compares the performance of 4 clustering algorithms: GMM, K-Medians, AP, and Gentic. The algorithms are clustering trasactional data from an Online UK Retail dataset. To evaluate each algorithm, VIKOR multi-criteria analysis was performed. The technique considered the following criteria for performance:
* Silhouette Score
* Calinski-Harabasz Index
* Davies-Bouldin Index
* Clustering Time
* Cluster Spread Index
* Size of the smallest cluster
* Standard deviation of cluster sizes
* Distinguishability of Revenue
Finally, the work performs an eda of the top performer's (K-medians k=2) cluster results to demonstrate the actionable insights that can be gained in a business context.

# How to Replicate the Results
Make sure the following packages are installed:
* pandas
* numpy
* statsmodels.api
* matplotlib
* statistics
* Sci-kit learns
* deap
* seaborn
* scipy
* psutil
* pygad
* topsisx
* pyclustering

Download the Online Retail.xlsx file and all of the xlsx files from the zip file see in the repository. The file mounts to your google drive to access these files. Each file has the following lines of code to read them into Google Colab:
```python
data = pd.read_excel('/content/drive/My Drive/Colab Notebooks/DS 340W/Online Retail.xlsx') # Online Retail Raw data file

train_split = pd.read_excel('/content/drive/My Drive/Colab Notebooks/DS 340W/data_train.xlsx') # Training set
val_split= pd.read_excel('/content/drive/My Drive/Colab Notebooks/DS 340W/data_val.xlsx') # Test set
test_split= pd.read_excel('/content/drive/My Drive/Colab Notebooks/DS 340W/data_test.xlsx') # Validation set
```
Either replicate the file paths by adding the appropriate folders in your Google Drive or change the file paths to match your current drive organization.

Once the file paths match your Google Drive organization, you will be able to run the colab file. 

**One important note, the Genetic clustering algorithm implementation is computationally expensive and does take about 12-15 minutes to run. We included a print() statement in the code that states which K-value in the for loop the file is currently running.

After about 15-20 minutes total, the entire colab file should have run with no errors.

