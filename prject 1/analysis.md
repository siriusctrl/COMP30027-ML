- Question 1

    - Information gain is a measure of how attribute values are correlated and how evenness of the class distribution changes. When IG of an attribute is low with respect to the class, the split might not good enough.
    - Based on the code results which I shown above, relatively higher IG tends to have a better performance on NB classifier.
    - However, some dataset are odd.
      - 

- Question 2

    - I've implemented the following evaluation method

        1. Full-test and full-train

        2. Hold-out (by default, 8-2 split, distributions are kept)

        3. Random sampling (by default, 8-2 split)

    - According to the results, method 2 and 3 are generally better than 1, since purely random sampling often results in different distribution setup in evaluation set. In this case, the occurrence or disappear of rare instance may leads to very different results. But in long run, it should leads to similar results as hold-out.

    - When comparing method 1 and 2, for dataset

        - In **hepatitis** (1/9), method 2 gives us a noticeable better results than method 1.
        -   In **anneal**, **cmc**, **hypothyroid**, **nursery** , **car**, **breast-cancer** and **mushroom** (7/9) gives us some very close results.
        - In **primary-tumor** (1/9), method 1 shows a significantly better result.

    - 