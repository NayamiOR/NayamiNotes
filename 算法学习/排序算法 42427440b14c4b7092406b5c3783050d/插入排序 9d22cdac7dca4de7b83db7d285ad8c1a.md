# 插入排序

把数据分成两组，一个有序序列一个无序序列，从无序序列中抽出一个与有序序列中的数据比较，插入到合适的位置，重复上述过程

这个过程很像扑克牌的理牌

一般来说很低效，在对几乎已经排好序的数据操作时效率很高

```c
void insertion_sort(int arr[], int len){
        int i,j,key;
        for (i=1;i<len;i++){
                key = arr[i];
                j=i-1;
                while((j>=0) && (arr[j]>key)) {
                        arr[j+1] = arr[j];
                        j--;
                }
                arr[j+1] = key;
        }
}
```

![%E6%8F%92%E5%85%A5%E6%8E%92%E5%BA%8F%209d22cdac7dca4de7b83db7d285ad8c1a/Untitled.png](%E6%8F%92%E5%85%A5%E6%8E%92%E5%BA%8F%209d22cdac7dca4de7b83db7d285ad8c1a/Untitled.png)