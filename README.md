## CBS_SVD and CBS_SVD_R

The fuctions will produce the rank 1 (CBS_SVD) or rank _r_ (CBS_SVD_R) sparse singular vectors for chosen cardinalities.

No additional R packages are reqired to run either CBS_SVD or CBS_SVD_R functions.

Function inputs:
  1. **X** : The similarity matrix created from the two datasets.
  2. SVDx : The sigular value decomposition results on **X** from the base R funtion svd().
  3. rank : The number of sigular vectors in each **u** and **v** (Default is rank=1).
  4. ku : The desired cardinality of the row variables of the similarity matrix (scalar if rank=1,     
           otherwise vector of length=rank).
  5. kv : The desired cardinality of the column variables of the similarity matrix (scalar if rank=1, 
          otherwise vector of length=rank).
  6. epsilon : The threshold of convergence to 1 in the inner product of the current sparse vector with its previous iteration (default is epsilon=0.05). 

# CBS_SVD
Function outputs:
  1. u : The rank 1 sparse vector for the similarity row variables.
  2. v : The rank 1 sparse vector for the similarity column variables.
  3. d : The first singular value.
  4. U.selected : The position values of the non zero elements of vector u. 
  5. V.selected : The position values of the non zero elements of vector v.

# CBS_SVD_R
Function outputs:
  1. epsilon : The convergence threshold use in the function.
  2. D : The first _r_ singular values where rank=_r_.
  3. ku : Vector of cardinalities of length=_r_ for the row variables of the similarity matrix.
  4. kv : Vector of cardinalities of length=_r_ for the column variables of the similarity matrix.
  5. U : Matrix of sparse vectors for the similarity row variables where the number of columns in this 
         matrix is equal to the chosen rank=_r_.
  6. V : Matrix of sparse vectors for the similarity column variables where the number of columns in 
         this matrix is equal to the chosen rank=_r_.
  7. U.selected : The position values of the non zero elements for each column of the matrix U. 
  8. V.selected : The position values of the non zero elements for each column of the matrix V.
  9. U.check : Matrix of inner products between all columns of matrix U.
  10. V.check : Matrix of inner products between all columns of matrix V.
