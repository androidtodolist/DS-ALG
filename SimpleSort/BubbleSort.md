# 冒泡排序  
### 一、特点：最大的数据项总是冒泡到数组的右边

    public void bubbleSort() {
        for (int out = intArray.length - 1; out > 0; out--) {
            for (int in = 0; in < out; in++) {
                if (intArray[in] > intArray[in + 1]) {
                    swap(in, in + 1);
                }
            }
        }
    }

### 二、效率：O(N²)
- 比较次数:约为N²/2   
(N-1)+(N-2)+(N-3)+...+1=N*(N-1)/2   

- 交换次数:平均为N²/4   
平均有一半的元素需要交换，最坏的情况:N²/2


