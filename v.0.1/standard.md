*Sprache is mailny inspired by C, ASM and [LBL](https://github.com/MrGargoyle134/lbl)*

## Constants
* string are marked by ```"``` 
* int are marked by ```(``` and ```)```

## Instructions

Each instruction is terminated by a ```;```.

### Blocks 

Blocks are delimited with  ```[``` and ```]```.

## Variables

Variables are marked like that by```/foo/```

You can define a new variable with the ```string``` and ```int``` keywords (see 
[keywords section](#-variables-definition-)).

## Keywords

Sprache allow to use some keywords, marked by ```:foo:```. 

### Set/ret :
* ```:set: /arg1/ /arg2/``` : set ```arg1``` to ```arg2```
* ```:ret: /arg1/```        : set ```arg1``` to the value returned by the last operation


### Operations :

* ```:add: /arg1/ /arg2/``` : return ```arg1```+```arg2```
* ```:sub: /arg1/ /arg2/``` : return ```arg1```-```arg2```
* ```:mul: /arg1/ /arg2/``` : return ```arg1```*```arg2```
* ```:div: /arg1/ /arg2/``` : return ```arg1```/```arg2```
* ```:lsh: /arg1/ /arg2/``` : return ```arg1```<<```arg2```
* ```:rsh: /arg1/ /arg2/``` : return ```arg1```>>```arg2```
* ```:and: /arg1/ /arg2/``` : return ```arg1```&```arg2```
* ```:or: /arg1/ /arg2/```  : return ```arg1```\|```arg2```
* ```:xor: /arg1/ /arg2/``` : return ```arg1```^```arg2```
* ```:not: /arg1/```        : return !```arg1```

### Comparison :
* ```:equal: /arg1/ /arg2/```  : return 1 if ```arg1```==```arg2```, else return 0
* ```:nequal: /arg1/ /arg2/``` : return 1 if ```arg1```!=```arg2```, else return 0
* ```:sup: /arg1/ /arg2/```    : return 1 if ```arg1```>```arg2```, else return 0
* ```:soe: /arg1/ /arg2/```    : return 1 if ```arg1```>=```arg2```, else return 0
* ```:inf: /arg1/ /arg2/```    : return 1 if ```arg1```<```arg2```, else return 0
* ```:ioe: /arg1/ /arg2/```    : return 1 if ```arg1```<=```arg2```, else return 0

### Condition :
* ```:if: /cond/ [code]```    : ```code``` is executed only if ```cond```=1
* ```:while: /cond/ [code]``` : ```code``` is repeted as long as ```cond```=1

### Variables définition :
* ```:int: /name/```    : create a ```int``` variable with the name ```name```
* ```:string: /name/``` : create a ```string``` variable with the name ```name```

## Functions

Functions are marked with ```<``` and ```>```.

### Definition :

Function are defined like that :
```<name> :type1: /arg1/ :type2: /arg2/
[
    code; 
]
```

### Call :
Call function like that :
```<name> /arg1/ /arg2/```

## Comments

Every thing that is not between ```()``` ; ```""``` ; ```::``` ; ```//``` ; ```<>``` or contain ```[``` ; ```]``` or ```;``` will be considered as a comment. 
