#### rmpalindrome
R package

## Remove Palindromic SNPs

### Description
Detect SNPs palindromic with palindromic alleles and remove them if their allele frequency is within a specific threshold around the allele frequency of 0.5.

### Usage
rm_palindrome(testData, t)

### Arguments

#### testData	
data.frame or data.table containing "reference_allele" and "other_allele" columns, each column contains single character (either A, T, G, or C). Note that the function uses rs_number to remove the SNPs from the original data.frame, making "rs_number" a required column.

#### t	
Threshold value >0 & <=0.5

### Value
data.table or data.frame with removed palindromic SNPs within 0.5 +/- threshold t (note that function must be called and assigned to a data.frame, see examples)

### Examples
result_df <- rm_palindrome(input_df,t);

result_df <- rm_palindrome(myData,0.2);

---

To install this package:

1. First, install the devtools package. Invoke R and then run:
```
install.packages("devtools")
```

2. Load the devtools package.
```
library(devtools)
```

3. Install the rmpalindrome package from GitHub:
```
install_github("urvashi-s/rmpalindrome")
```

And voila! Happy coding :)
