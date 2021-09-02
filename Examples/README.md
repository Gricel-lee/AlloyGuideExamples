# Integers

- Code with error:

![image](https://user-images.githubusercontent.com/63869574/131929567-4ecb7878-6f18-45e0-9536-40447723f490.png)

- Fixed one:

![image](https://user-images.githubusercontent.com/63869574/131929572-6970e014-aaa4-4a9a-9fe1-890bd5d6c827.png)


- Evaluation test: 

![image](https://user-images.githubusercontent.com/63869574/131929758-ca7eb57d-7d19-4932-871e-2e3096847e7d.png)



- Another useful example...

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
sig sumab{
	value : Int
}
{
value = plus[a.value, b.value]
}
run add for 10 int, exactly 1 sumab, exactly 1 a, exactly 1 b
```

- Visualizing the model found:
 
![image](https://user-images.githubusercontent.com/63869574/131930545-d4c74842-62f6-4bad-9299-bf9d7ffe57c5.png)
