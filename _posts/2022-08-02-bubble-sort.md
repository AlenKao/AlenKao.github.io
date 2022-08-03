---
title: 泡沫排序法
tags: algorithm
show_subscribe: false
---
Bubble sort
<!--more-->
## 時間複雜度
~~~
泡沫排序對n個項目需要O(n^2)的比較次數，且可以原地排序。   
儘管這個演算法是最簡單瞭解和實作的排序演算法之一，但它對於包含大量的元素的數列排序是很沒有效率的。
~~~   
## 泡沫排序演算法的運作如下：
~~~
1. 比較相鄰的元素。如果第一個比第二個大，就交換它們兩個。
2. 對每一對相鄰元素作同樣的工作，從開始第一對到結尾的最後一對。這步做完後，最後的元素會是最大的數。   
3. 針對所有的元素重複以上的步驟，除了最後一個。   
4. 持續每次對越來越少的元素重複上面的步驟，直到沒有任何一對數字需要比較。
~~~

程式碼範例 `C++`
------
```c++
template<typename T>
void bubble_sort(T arr[], int len) {
	int i, j;
	for (i = 0; i < len - 1; i++)
		for (j = 0; j < len - 1 - i; j++)
			if (arr[j] > arr[j + 1])
				swap(arr[j], arr[j + 1]);
}
```

[參考資料](https://zh.wikipedia.org/wiki/%E5%86%92%E6%B3%A1%E6%8E%92%E5%BA%8F#C++)