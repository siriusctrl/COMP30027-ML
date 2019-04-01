- Question 1

    - Information gain is a measure of how attribute values are correlated and how evenness of the class distribution changes. When IG of an attribute is low with respect to the class, the split might not good enough.
    - Based on the code results which I shown above, relatively higher IG tends to have a better performance on NB classifier. Since it is much easier for the classifier to distinguish them from each other.
    - However, some dataset are odd.
      - For dataset hypothyroid.csv, although it has a relatively low IG but it is only a two labels classifier and it has enough instance, so the acc still remains pretty high.
      - For dataset primary-tumor.csv, it has two very high IG but the reason for that is it contain a huge proportion of missing values for those two features. Therefore, acc remains low.

- Question 4

    - I've implemented the following evaluation method

        1. Full-test and full-train

        2. Hold-out (by default, 8-2 split, distributions are kept)

    - When comparing method 1 and 2, for dataset

        - In **hepatitis** (1/9), method 2 gives us a noticeable better results than method 1.
        - In **primary-tumor** (1/9), method 1 shows a significantly better result.
          - The main reason for these two difference in acc are both caused by lack of instance. 
            - For primary-tumor, some attributes have a large proportion of missing data which cannot be neglected, especially for column 'degree-of-diffe'. Also, regarding to the IG hundreds of data is not enough to learn 21 possible labels. The lack of instance is very hard for NB to learn the model, therefore, method 1 will trends to over-estimated.
            - For hepatitis, it may caused by biased data.
        - In **anneal**, **cmc**, **hypothyroid**, **nursery** , **car**, **breast-cancer** and **mushroom** (7/9) gives us some very close results.
          - The dataset is large enough to learn the pattern within the dataset. As we keep the distribution of data when extracting training data from the dataset, the performance (acc) are hardly be affected. 