# Java003: Object-Oriented Programming

## Differences between **Object-Oriented Programming** and **Procedural Programming**
- In procedural programming, it is just like a sequence of instructions, focusing only on **what to do** step by step.

- However, in object-oriented programming, programs are objects that combined with data and behaviors, focusing on who owns the data and what they can do.

## Relations Between Class, Objects and Methods
### Class
- Class: a template
- Object: an instance of a class
- Method: a function belonging to a class/object

Here is a general form of class:
```
class ClassName{

    //instance variable
    Type varName;

    //constructor
    classNme(parameters){
        // initialization code
    }

    //method
    ReturnType methodName(parameters){
        // method body
    }
}
```

## Copy by Value & Copy by Reference
1. Copy by **value**
    - Here is an example of copy by value. After the `x` copied the value of `y`, the `y` was modified. In this case, x will remain the original value of `y` instead of changing with the reassignment of `y`.
```
int x = 6;
int y = 9;

x = y;
y = 3;
```

2. Copy by reference
    - Although the code below is really similar to the example for copy by value, it turns out to be significantly different. In this case, the address of `bill` is copied by `andy`. The change of age of `andy` will reflect on `bill`'s age.
```
Elephant bill = new Elephant();
bill.age = 10;

Elephant andy = new Elephant();
andy.age = 1;

andy = bill;

andy.age = 5;
```
### Method
A `Method` defines the behaviors of a `class`, it operates on the object's data and hides implement details.

## Garbage Collection
Compared with some programming language such as `C`, `Java` has is smarter when it comes to memory management. It can manage memory automatically.

**Garbage Collection** is a feature of `Java`. Specifically, if no reference point to an object, it becomes eligible for garbage collection. 