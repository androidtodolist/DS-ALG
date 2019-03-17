# 二分查找 
### 一、二分法查找适用于数据量较大时，但是数据需要先排好顺序。

### 二、代码    
    public int binarySearch(int searchkey) {
        int lowerBound = 0;
        int upperBound = intArray.length - 1;
        int currentIndex;
        while (true) {
            currentIndex = (lowerBound + upperBound) / 2;
            if (intArray[currentIndex] == searchkey) {
                return currentIndex;
            } else if (lowerBound > upperBound) {
                return -1;
            } else {
                if (intArray[currentIndex] < searchkey) {
                    lowerBound = currentIndex + 1;
                } else {
                    upperBound = currentIndex - 1;
                }
            }
        }
    }

### 三、算法复杂度
-   时间复杂度  
1.  最坏情况查找最后一个元素（或者第一个元素）Master定理T(n)=T(n/2)+O(1)所以T(n)=O(log2n)
2.  最好情况查找中间元素O(1)查找的元素即为中间元素（奇数长度数列的正中间，偶数长度数列的中间靠左的元素）
-   空间复杂度  
S(n)=n


