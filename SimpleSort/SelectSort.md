# 选择排序  
### 一、特点：
-   选择一个标兵
-   最小的数据项总是交换到数组的左边

### 二、代码
    public void selectSort() {
        //out选择标兵
        for (int out = 0; out < intArray.length - 1; out++) {
            int min = out;
            //in找到剩余未排序部分最小值
            for (int in = out + 1; in < intArray.length; in++) {
                if (intArray[in] < intArray[min]) {
                    min = in;
                }
            }
            swap(out, min);
        }
    }


### 三、效率：O(N²)
- 比较次数:约为N²/2   
(N-1)+(N-2)+(N-3)+...+1=N*(N-1)/2   

- 交换次数：最多N-1次     
- 交换数据比较比较实际级别大的多的时候，选择排序相当快。


