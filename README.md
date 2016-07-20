# README-EDITS - Branch:readme-edits

# datacamp.com-courses-intermediate-r-chapter-1-conditionals-and-control-flow-r
https://www.datacamp.com/courses/intermediate-r/chapter-1-conditionals-and-control-flow-r

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
>  
