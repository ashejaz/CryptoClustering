## Overview

For this project, unsupervised machine learning techniques were deployed to cluster changes in cryptocurrencies.

The following data was imported into a Pandas DataFrame:

<img width="836" alt="Screenshot 2023-09-04 at 15 00 35" src="https://github.com/ashejaz/CryptoClustering/assets/127614970/ba467dc0-4f60-4d3f-a824-97e328e0efe4">

## Data Scaling

The StandardScaler() module from scikit-learn was then used to scale the data. 

The following scaled DataFrame was created:

<img width="813" alt="Screenshot 2023-09-04 at 15 00 48" src="https://github.com/ashejaz/CryptoClustering/assets/127614970/675ada25-9c3b-4c1a-aa5f-62ae6e375088">

## Exploration of scaled data

The *elbow method* was used to determine the ideal number of clusters. From the plot, it can be observed that the optimal k value is 4.

<img width="728" alt="Screenshot 2023-09-04 at 14 57 20" src="https://github.com/ashejaz/CryptoClustering/assets/127614970/5157d189-cdaf-4777-b3f8-cd47fcfbb8e9">


A *K-means model* was then used to cluster the data based on the ideal k-value of 4. The following scatter plot was created:

<img width="727" alt="Screenshot 2023-09-04 at 14 57 31" src="https://github.com/ashejaz/CryptoClustering/assets/127614970/2a827aba-ca8a-49c3-a4fa-78b7fa578796">

We can observe 2 main clusters with the currencies in red and yellow appearing to be outliers.


## Principal Component Analysis

A PCA was then performed on the scaled data to reduce the number of features to three principal components.

The following DataFrame was created:

<img width="288" alt="Screenshot 2023-09-04 at 15 01 21" src="https://github.com/ashejaz/CryptoClustering/assets/127614970/4086e603-f37b-4375-87a8-815201f6620e">

The elbow method was then used on this data to once again determine the best value for k.

<img width="789" alt="Screenshot 2023-09-04 at 14 57 42" src="https://github.com/ashejaz/CryptoClustering/assets/127614970/a56b7b7c-cb70-4459-8ebf-7b6d82a6d6a1">

This was found to be 4, the same value as when the method was performed on the original scaled data.

K-means clustering yielded the following scatter plot:

<img width="713" alt="Screenshot 2023-09-04 at 14 57 57" src="https://github.com/ashejaz/CryptoClustering/assets/127614970/cbc41adb-fcd2-4f14-91ad-31a3d7e31a6e">

## Conclusions

PCA did not give a different ideal k-value compared with the original scaled data.

<img width="728" alt="Screenshot 2023-09-04 at 14 57 20" src="https://github.com/ashejaz/CryptoClustering/assets/127614970/f5e5ccae-212c-474b-b4a3-c615a2923d66">
<img width="789" alt="Screenshot 2023-09-04 at 14 57 42" src="https://github.com/ashejaz/CryptoClustering/assets/127614970/c215f0a9-d164-4029-8461-4b778f1e86c3">

However, by reducing the features to 3, the clusters become more distinct and it is easier to see 'celsius-degree-token" as a separate/outlying datapoint. Though the PCA clusters were cleaner and easier to visualise, the overall results were similar to the clusters formed from the original scaled data. The benefits of using fewer features may be better demonstrated with a larger dataset.

<img width="727" alt="Screenshot 2023-09-04 at 14 57 31" src="https://github.com/ashejaz/CryptoClustering/assets/127614970/8d6af361-e8b0-45da-89dc-e185ac9e9043">
<img width="713" alt="Screenshot 2023-09-04 at 14 57 57" src="https://github.com/ashejaz/CryptoClustering/assets/127614970/bbef5feb-3d0b-408d-9d3b-f1c3a82b0bff">

## Files

The raw data can be found in CSV format [here](Resources/crypto_market_data.csv).

The jupyter notebook containing the analysis can be found [here](Crypto_Clustering.ipynb).

## References

The data used in this project was generated for edX Bootcamps LLC.
