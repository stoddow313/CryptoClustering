# CryptoClustering

## Background and Information: 

This challenge was presented to us to utilize our knowledge of Python, and unsupervised learning to predict if cryptocurrencies are affected by price changes over different time periods. We were provided a csv file that included all the datapoints we needed to reference, and then given a starter_code which was renamed to hold all the coding that was done. Below is a short synopsis of the process to completing this challenge. 

## Part 1: Prepare the Data

In this section of the challenge, I was tasked with using StandardScaler from our scikit-learn to normalize the data in the CSV file that was read in using pandas. Once we normalized the data and scaled it, it was placed into a Dataframe and an index called "coin_id" was added. 

## Part 2: Original Scaled K Value and Plotting

In this section I utilized the original dataframe that was created in the above part to find our best K value. To do so, I started by creating a list of k values ranging from 1 to 11, and making an empty list for our inertia values. Then I proceeded to compute our inertia with each possible value of K by running a for loop that appended our empty inertia list until it was completely full. Afterwards, a dictionary with our data was created to then create our elbow curve. In this part we found that the best value of k was 4. Finally we took that k value of 4 and used it to initialize our Kmeans model. We fit the model, and then predicted our clusters using the original scaled data. Once we had the predicted clusters we were able to create a copy of our dataframe, add the cluster to it, and create a scatterplot using those values. 

## Part 3 & 4: Using PCA data. 

Both of these sections were the exact same as above except we were now using PCA versions of our data. We did find that the best k value using PCA data was still 4 and used that to create another scatterplot which was then compared to our original. It was found that when using PCA data which has less variables in it, our clusters were tighter together than in the original scatterplot. 