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

### Dot and box join
In the following example, we have "Book.address":
```
Book.address = {(N0, A0), (N1, A0), (N2, A2)}
myName = {(N1)}
Book.address[myName] = {(A0)}
Book.address.myName = {}
```
The last two results are different because [myName] looks for relations from ```Book.address``` where the first part is "myName". This is ```(N1,A0)```, hence the mapping returns ```A0```. 
However, when writing ```Book.address.myName```, we are looking for a map from ```Book.address``` to myName, hence, it looks for ```A0,A0,A2``` in ```N1```, which leads to nothing.


![image](https://user-images.githubusercontent.com/63869574/231194173-5f932490-502b-4783-bb39-5fe8302f566b.jpeg)
