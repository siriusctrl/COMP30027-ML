- Question 1
    - Based on the code results which I shown above, relatively higher IG tends to have a better performance on NB classifier. Since it is much easier for the classifier to distinguish them from each other.
    - However, some dataset are odd.
      - For dataset hypothyroid.csv, although it has a relatively low IG but it is only a two labels classifier and it has enough instance, so the acc still remains pretty high.
      - For dataset primary-tumor.csv, it has two very high IG but the reason for that is it contain a huge proportion of missing values for those two features. Therefore, acc remains low.
- Question 4
  - I've implemented the following evaluation method
    1. Full-test and full-train
    2. Hold-out (by default, 8-2 split, distributions are kept)
    3. random Sampling (by default, 8-2 split, distributions are not kept)
  - When comparing method 1 and 2, for dataset
    - For most of the dataset, the acc for different methods are in the similar range. Those datasets are large enough to learn the pattern within the datasets. As we keep the distribution of data when extracting training data from the dataset, the performance (acc) are hardly be affected. 
    - Specific dataset yield some interesting results
      - Breast-cancer and hepatitis
        - Although they got quite similar results in acc for method 1 and method 2. The acc for method 2 seems varying in a quite large range. One of the reason is that small number of instance. As the distributions are kept, another reason for this is that the data are biased.
      - Primary-tumor
        - For this dataset, missing values take a huge count in why method 1 has significant larger acc (refer to the missing value that I printed out for each attribute above). Lacking of instance also becomes a problem here.