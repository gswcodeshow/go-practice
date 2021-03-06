##   桶排的优化
---
##### 问题描述
给出一个100的数组，里面存放着0-100的数字，且唯一不重复，请实现一个算法在不使用额外的存储空间和基本的排序算法的情况下，实现对100数组的排序。
---
##### 解题思路
首先想到的就是开辟一个新的100空间，让后循环一遍就可以达到排序的效果，但是按照要求并不可以直接开辟空间，所以通过递归交换的方式，也可以达到相同的效果。
---
#### 源代码参考
```
func sort(start *[100]int) [100]int {
	for i := 0; i < 100; i++ {
		for {
			if i != start[i] {
				start[i], start[start[i]] = start[start[i]], start[i]
				continue
			}
			break
		}
	}
	return *start
}
```






