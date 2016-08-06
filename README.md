# Construct a matrix with 3 rows that contain the numbers 1 up to 9
matrix(1:9, byrow=TRUE,nrow=3)
> matrix(1:9,byrow=TRUE,nrow=3)
     [,1] [,2] [,3]
[1,]    1    2    3
[2,]    4    5    6
[3,]    7    8    9

# README-EDITS - Branch:readme-edits - GITHUB GUIDES

# datacamp.com-courses-intermediate-r-chapter-1-conditionals-and-control-flow-r
https://www.datacamp.com/courses/intermediate-r/chapter-1-conditionals-and-control-flow-r

## EQUALITY ##
## The most basic form of comparison is equality. Let's briefly recap its syntax. The following statements all evaluate to TRUE (feel free to try them out in the console).
> # Comparison of logicals
> TRUE==FALSE
[1] FALSE
> 
> # Comparison of numerics
> -6*14!=17-101
[1] FALSE
> 
> ## Comparison of character strings
> "useR"=="user"
[1] FALSE
> 
> # Compare a logical with a numeric
> TRUE==1
[1] TRUE
 
      [,1]  [,2]  [,3]  [,4]  [,5]  [,6] [,7]
[1,] FALSE FALSE  TRUE FALSE FALSE FALSE TRUE
[2,] FALSE FALSE FALSE FALSE FALSE  TRUE TRUE
## EQUALITY - REPEATED ##
> # Comparison of logicals
> TRUE==FALSE
[1] FALSE
> 
> # Comparison of numerics
>  -6*14!=17-101
[1] FALSE
> 
> # Comparison of character strings
> "useR"=="user"
[1] FALSE
> 
> # Compare a logical with a numeric
> TRUE==1
[1] TRUE
# GREATER AND LESS THAN ##
> # Comparison of numerics
> -6*5+2>=-10+1
[1] FALSE
> 
> # Comparison of character strings
> "raining"<="raining dogs"
[1] TRUE
> 
> # Comparison of logicals
> TRUE>FALSE
[1] TRUE
## COMPARE VECTORS ##
>   # The linkedin and facebook vectors have already been created for you
> linkedin <- c(16, 9, 13, 5, 2, 17, 14)
> facebook <- c(17, 7, 5, 16, 8, 13, 14)
> 
> # Popular days
> linkedin>15
[1]  TRUE FALSE FALSE FALSE FALSE  TRUE FALSE
> 
> # Quiet days
> linkedin<=5
[1] FALSE FALSE FALSE  TRUE  TRUE FALSE FALSE
> 
> # LinkedIn more popular than Facebook
> linkedin>facebook
[1] FALSE  TRUE  TRUE FALSE FALSE  TRUE FALSE
## COMPARE MATRICES ##
> # The social data has been created for you
> linkedin <- c(16, 9, 13, 5, 2, 17, 14)
> facebook <- c(17, 7, 5, 16, 8, 13, 14)
> views <- matrix(c(linkedin, facebook), nrow = 2, byrow = TRUE)
> 
> # When does views equal 13?
> views==13
      [,1]  [,2]  [,3]  [,4]  [,5]  [,6]  [,7]
[1,] FALSE FALSE  TRUE FALSE FALSE FALSE FALSE
[2,] FALSE FALSE FALSE FALSE FALSE  TRUE FALSE
> 
> # When is views less than or equal to 14?
> views<=14
      [,1] [,2] [,3]  [,4] [,5]  [,6] [,7]
[1,] FALSE TRUE TRUE  TRUE TRUE FALSE TRUE
[2,] FALSE TRUE TRUE FALSE TRUE  TRUE TRUE

## & and | ##
# The linkedin and last variable are already defined for you
> linkedin <- c(16, 9, 13, 5, 2, 17, 14)
> last <- tail(linkedin, 1)
> 
> # Is last under 5 or above 10?
> last<5|last>10
[1] TRUE
> 
> # Is last between 15 (exclusive) and 20 (inclusive)?
> 15<last&last<=20
[1] FALSE

## & and |(2) ##
# linkedin exceeds 10 but facebook below 10
> 10<linkedin&10>facebook
[1] FALSE FALSE  TRUE FALSE FALSE FALSE FALSE
> 
> # When were one or both visited at least 12 times?
> 12<=linkedin|12<=facebook
[1]  TRUE FALSE  TRUE  TRUE FALSE  TRUE  TRUE
> 
> # When is views between 11 (exclusive) and 14 (inclusive)?
> 11<views&views<=14

## Blend It All Together ##
> # li_df is pre-loaded in your workspace
> 
> # Select the second column, named day2, from li_df: second
> li_df$day2
 [1]  3 23 18 18 25 20  4  3 22 12 27 13 17 27  6 35 17  6  1 12 15 17 12  8  7
[26] 25 15 32 29  1 22 11  5 17 12 26 13 10 37 33 19 29  8 22 10 19 27 18 15 28
> 
> # Build a logical vector, TRUE if value in second is extreme: extremes
> second <-(li_df$day2)
> 
> # Count the number of TRUEs in extremes
> extremes <- (second>25 | second<5)
> 
> # Solve it with a one-liner
> sum(extremes)
[1] 16
