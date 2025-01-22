##1.Concept : Basic operations on Matrices:
# Define mat1
mat1.data <- c(1, 2, 3, 4, 5, 6, 7, 8, 9)
mat1 <- matrix(mat1.data, nrow = 3, ncol = 3, byrow = TRUE)
mat1
# Define mat2
mat2.data <- c(10, 11, 12, 13, 14, 15, 16, 17, 18)
mat2 <- matrix(mat2.data, nrow = 3, byrow = TRUE)
mat2
# Access specific elements and subsets of mat2
mat2[1, 2]
mat2[c(1, 3), c(2, 3)]
# Drop row and column subsets
mat2[2, , drop = FALSE]
mat2[-1, -c(2, 3), drop = FALSE]
# Boolean indexing
mat2[c(TRUE, FALSE, TRUE), c(FALSE, TRUE, TRUE)]
# Perform scalar operations on mat1
mat1 * 5
mat1 + 2
mat1 / 2
# Define mat3 for matrix operations
mat3 <- matrix(1, nrow = 3, ncol = 3)
# Matrix arithmetic
mat_add <- mat1 + mat3
mat_add
mat_sub <- mat1 - mat3
mat_sub
mat_mul <- mat1 * mat3
mat_mul





##2.Concept : Multiplying a vector with a constant Adding two vectors
#Multiplying two vectors Subtraction
#Division operations on vectors Vectors sequence
#Repetition of vectors

# Create a vector and display it
vec1 <- c(1, 2, 3, 4, 5)
vec1
# Multiply each element of vec1 by 2
multivec <- vec1 * 2
multivec
# Create another vector
vec2 <- c(6, 7, 8, 9, 10)
# addition and multiplication
vector_add <- vec1 + vec2
vector_mul <- vec1 * vec2
vector_mul
#Subtraction and division
vector_sub <- vec2 - vec1
vector_sub
vector_div <- multivec / vec1
# Generate a sequence of 30 values between 1 and 20
vec_seq <- seq(from = 1, to = 20, length = 30)
vec_seq
# Repeat the values 2, 3, and 4 three times
vec_rep <- rep(c(2, 3, 4), times = 3)
vec_rep
# Calculate the sum of elements in vec_rep
sum(vec_rep)







##4.Random Number Generator In R.

#Create the data frame
df <- data.frame(
  "Serial_number" = 1:5, 
  "Age" = c(20, 21, 17, 23, 19), 
  "Name" = c("raja", "ramu", "ravi", "raghu", "rajesh")
   )
# Sort by age in ascending order
newdataAsc <- df[order(df$Age),]
newdataAsc
# Sort by age in descending order
newdataDsc <- df[order(-df$Age),]
newdataDsc






##6.Factorial Using Recursive Function

rec_fac <- function(x){ 
  if(x==0 || x==1){ 
    return(1)
   } else { 
    return(x*rec_fac(x-1))
   }
}
var <- readline(prompt = "Enter a number: ")
var = as.integer(var) 
print(var)
x<-var
f<-rec_fac(x)
t1<-c("factorial",x,"is",f )
t1










##8.Plot the Graph for Normal Distribution

# Create a sequence of numbers between -5 and 5 increment it by 0.2.
x <- seq(-5, 5, by = .1)
# The mean here is 1.0 and standard deviation as 0. 
y <- dnorm(x, mean =0, sd = 1)
#Plot the Graph 
plot(x,y)






##9.Time Series Graph For A Given Set Of Data

sales_ice <- c(450, 613, 466, 205.7,571.0, 622.0, 851.4, 621.4,875.3,979.7, 927.5,14.45)
sales_cooldrink <- c(550, 713, 566, 687.2,110, 120, 72.4,814.4,423.5, 98.7, 741.4,345.3)
combined.sales <- matrix(c(sales_ice,sales_cooldrink),nrow = 12)
sales.timeseries <- ts(combined.sales,start = c(2021,1),frequency = 12)
plot(sales.timeseries, main = "Showing ice cream – cooldrink sales")
print(sales.timeseries)

