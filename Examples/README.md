# Integers

- Code with error:

![image](https://user-images.githubusercontent.com/63869574/131929567-4ecb7878-6f18-45e0-9536-40447723f490.png)

- Fixed one:

![image](https://user-images.githubusercontent.com/63869574/131929572-6970e014-aaa4-4a9a-9fe1-890bd5d6c827.png)


- Evaluation test: 

![image](https://user-images.githubusercontent.com/63869574/131929758-ca7eb57d-7d19-4932-871e-2e3096847e7d.png)

Figure 1.


- Another useful example is the next one. Notice that there are two "sums" done (see Figure 2):
	- **sig abc** with __value= a.value + b.value + c.value__ . This means that abc.value from abc is a relation to the elements a.value, b.value and c.value.
	- **sig sumab** with __value = plus[a.value, b.value]__ . This means that sumab.value is the sum of the integers a.value and b.value.

```javascript
open util/integer

sig a{value: Int}
{
value = 4
}
sig b{value: Int}
{
value = 1
}
sig c{value: Int}
{
value = 3
}
sig abc{value: set Int}
{
	value = a.value + b.value + c.value
}

sig sumab{
	value : Int
}
{
value = plus[a.value, b.value] // same as:  value=a.value.plus[ b.value]
}

pred add{}

run add for 4 int, exactly 1 sumab, exactly 1 a, exactly 1 b, exactly 1 c, exactly 1 abc
```

- Visualizing the model found:
 
![image](https://user-images.githubusercontent.com/63869574/132242713-e9d61423-6524-4ac4-86b5-bd4c83056700.png)
Figure 2. 


For the sum of a set of integers, use **sum**:

```javascript
sig a{value: set Int}
{
value = {int 3 + int 2 + int 4}
}


sig suma{
	value : Int
}
{value = sum[a.value] }

pred add{}

run add for 5 int, exactly 1 suma, exactly 1 a```
