# 插入排序  
### 一、代码
    public void insertSort() {
        //out选择标兵
        for (int out = 1; out < intArray.length; out++) {
            //选择的标兵
            int temp = intArray[out];
            int in = out;
            while (in > 0 && intArray[in - 1] >= temp) {
                intArray[in] = intArray[in - 1];
                --in;
            }
            intArray[in] = temp;
        }
    }

### 二、效率：O(N)
- 比较次数:
最多:
(N-1)+(N-2)+(N-3)+...+1=N*(N-1)/2   
平均：
N*(N-1)/4
- 交换次数:  
大致等于比较的次数

- 对于随机无序数据也需要O(N²)时间级
- 对于有序和基本有序的数据，while循环条件总是假，变成了只有外层循环，执行N-1次，所以为O(N)

