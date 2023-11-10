# 1

# 2

- 取整 `round(3.1415926, 2)` = 3.14
- 绝对值误差 `abs_error <- abs(3.1415926 - 3.14)` = 0.0015926
- 相对误差 `relative_error <- (abs_error / 3.1415926) * 100` = 0.0507%
- 输出方式
  - `cat("pi = ", pi, "\n")`
  - `print(pi)`
  - `paste("pi = ", pi, "\n")`

# 3

- `x <- 5:15`
- `length(x)` = 11
- `x[1:5]` = 5 6 7 8 9
- `x[1:5] <- 1:5`
- `x` = 1 2 3 4 5 10 11 12 13 14 15
- `x[-3]` = 1 2 4 5 10 11 12 13 14 15
- `x[c(1, 3, 8)]` = 1 3 12
- `x[x > 10]` = 11 12 13 14 15
- `x[x > 10 & x < 14]` = 11 12 13
- `x[x > 10 | x < 14]` = 1 2 3 4 5 11 12 13 14 15
- 这里x是向量，所以可以直接用`x > 10`，但是如果是矩阵，就要用`x[, 1] > 10`，表示矩阵的第一列大于10
- `A <- rbind(c(1, 2, 3), c(4, 5, 6))`
- `A` = 1 2 3 </br>
        4 5 6
- `A[1, 2]` = 2
- `A[1, ]` = 1 2 3
- `A[, 2]` = 2 5
- `A[1:2, 2:3]` = 2 3 </br>
                  5 6
- `dim(A)` = 2 3
- `nrow(A)` = 2
- `ncol(A)` = 3

# 4

- 算次方 `a^2` `a ** 2`
- 算对数 `log10(477)`
- 类型 `class(a)` 得出的是 `numeric` `matrix` 这类的
- `typeof(a)` 得出的是里面具体的数的类型 `integer` `double`

# 5

- string `a <- "hello"`
- number `b <- 123`
- vector `c <- c(1, 2, 3)`
- matrix `d <- matrix(c(1, 2, 3, 4), nrow = 2, ncol = 2)`
- logical `e <- TRUE`
- list `f <- list(a, b, c, d, e)`

# 6 怎么用seq

- `seq(1, 10, by = 2)` = 1 3 5 7 9
- `seq(1, 10, length = 5)` = 1 3.25 5.5 7.75 10
- `mean(seq(1, 10, by = 2))` = 5
- `sum(seq(1, 10, by = 2))` = 25
- `prod(seq(1, 10, by = 2))` = 945 这个表示乘积

# 7 关于函数使用

- `f <- function(x) {x^2}`
- `f(2)` = 4

# 8 关于矩阵

- `M1=matrix(c(2,2.4,2.7,100.1,1i,as.integer(9)),nrow=2,ncol=3, byrow=TRUE)`
- `M1` = 2 2.4 2.7 </br>
        100.1 0+1i 9
- 这里 `byrow=TRUE` 表示按行填充，`byrow=FALSE` 表示按列填充
- `M2=matrix(c(2,2.4,2.7,100.1,1i,as.integer(9)),nrow=2,ncol=3, byrow=FALSE)` 默认是 `byrow=FALSE`
- `M2` = 2 2.7 1i </br>
        2.4 100.1 9

# 9 data.frame

    > df <- data.frame(
      Power = c(1, 2, 3, 4),
      Python = c(5, 6, 6, 6),
      Equations = c(9, 10, 123456789, 12)
    )
    > df
      Power Python Equations
    1     1      5         9
    2     2      6        10
    3     3      6 123456789
    4     4      6        12

# 10 循环 repeat

    > i <- 1
    > repeat {
      print(i)
      i <- i + 1
      if (i > 10) {
        break
      }
    }
    [1] 1
    [1] 2
    [1] 3
    [1] 4
    [1] 5
    [1] 6
    [1] 7
    [1] 8
    [1] 9
    [1] 10

# 11 画图


    x_a <- seq(-3, 3, by = 0.5)
    y_a <- x_a^3 - 2 * exp(x_a) + x_a

    x_b <- seq(-3, 3, by = 0.1)
    y_b <- x_b^3 - 2 * exp(x_b) + x_b

    x_c <- seq(0, 3, by = 0.1)
    y_c <- sqrt(x_c) + 6


    plot(x_a, y_a, type = "l", col = "blue", xlab = "x", ylab = "f(x)", ylim=c(-30,10), main = "Plot of f(x) = x^3 - 2e^x + x")

    lines(x_b, y_b, col = "red")
    lines(x_c, y_c, col = "green")

# 12 for循环

    > for (i in 1:10) {
      print(i)
    }
    [1] 1
    [1] 2
    [1] 3
    [1] 4
    [1] 5
    [1] 6
    [1] 7
    [1] 8
    [1] 9
    [1] 10

# 13 for循环的seq_alone

    > c1 <- 1:10
    for (i in seq_along(c1)) {
      print(i)
    }
    [1] 1
    [1] 2
    [1] 3
    [1] 4
    [1] 5
    [1] 6
    [1] 7
    [1] 8
    [1] 9
    [1] 10