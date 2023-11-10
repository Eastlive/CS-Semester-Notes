# 1 func

# 2 funk

# 3 判断是不是矩阵

- is.matrix(X) == True

# 4 hans

# 5 hashu

# 6

# 7 intersect()

    x = c(10, 20, 30, 20, 20, 25, 29, 26)
    y = c(10, 50, 30, 20, 20, 35, 19, 56)
    z = c(10, 40, 30, 20, 20, 25, 49, 26)

    intersect(x,intersect(y,z))

# 8 进制转换

    library("bigBits")
    base2base(45,frombase = 10, tobase=16)

# 9 信息熵 entropy

    entropy <- function(x) {
      x <- as.numeric(x)
      x <- x/sum(x)
      -sum(x * log(x))
    }

    entropy(c(1,2,3,4,5,6,7,8,9,10))

- 公式 entropy
$$H(X) = -\sum_{i=1}^n p(x_i) log p(x_i)$$

- ACL (Average code length) 平均code长度
$$ACL_{C} = \sum_{i=1}^n p(x_i) L(x_i)$$

# 10 Huffman Code

- compress <- paste0(compress, code[j])

- 步骤
    1. 计算每个字符的频率
    2. 按照频率从小到大排序
    3. 选取频率最小的两个字符，合并为一个节点，频率为两个节点的频率之和
    4. 重复3，直到只剩下一个节点
    5. 从根节点开始，左子树为0，右子树为1，得到每个字符的编码