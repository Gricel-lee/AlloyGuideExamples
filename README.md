# AlloyGuideExamples
Examples and solutions to problems encountered when using Alloy and Alloy Analyzer - https://alloytools.org/ 





## Logic relational 
In Alloy, relations can be done using the dot operator. In the following example, "p." means:
```
a->b
a->c
b->d
```
then we use the relations in q to get "p.q":
```
a-> b ->c,c
a-> b ->a,d
a-> c ->c,c
b-> d -> no mapping
```

![image](https://user-images.githubusercontent.com/63869574/231190713-a14c6de8-0afd-4ec6-8998-fb808af42a5e.jpeg)


![image](https://user-images.githubusercontent.com/63869574/231194173-5f932490-502b-4783-bb39-5fe8302f566b.jpeg)
