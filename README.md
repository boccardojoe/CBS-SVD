# CBS_SVD and CBS_SVD_R
No additional R packages are reqired to run either CBS_SVD or CBS_SVD_R functions.
Function inputs:
  1. **X** : The similarity matrix created from the two datasets.
  2. SVDx : The sigular value decomposition results on **X** from the base R funtion svd().
  3. rank : The number of sigular vectors in each **u** and **v** (Default is rank=1).
  4. ku : The desired cardinality of the row variables of the similarity matrix (scalar if rank=1, otherwise vector of length=rank).
  5. kv : The desired cardinality of the column variables of the similarity matrix (scalar if rank=1, otherwise vector of length=rank).
  6. epsilon : The threshold of convergence to 1 in the inner product of the current sparse vector with its previous iteration (default is epsilon=0.05). 


Function outputs:
  1. 
