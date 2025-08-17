## **Assignment No : 01**

## **Assignment Name : Inheritance in C++**

## **Submission Date : May 19, 2025**

## Code :
```C++
#include<bits/stdc++.h>
using namespace std;

class A{
    int size;
    public:
        int price;
    protected:
        int total;
};

class B: public A{
    int roll;
    public:
        int id;
    protected:
        int salary;
};

class C: public B{
    int number;
    public:
    void f(){cout << "This is C";};
    protected:
    string s;
};
int main()
{
    A ob1;
    B ob2;
    C ob3;

    ob1.price = 10;
    ob2.price = 20;  
    ob2.id = 30;
    ob3.price = 40;
    ob3.id = 50;     
    ob3.f();

    ob1.total = 100;
    ob2.total = 100;
    ob3.salary = 6000;
    ob3.total = 70;
    ob1.size = 1;
    ob2.roll = 2;
    ob3.number = 3;
    ob3.s = "Nahed";
}

```
After running several times, C can only access public members from B and A. B can only access public members from A. A can not access B or C members.
## **Output :** 
<img width="1226" height="834" alt="image" src="https://github.com/user-attachments/assets/11e31269-2d87-4dce-ad73-18678e642875" />
<img width="1238" height="765" alt="image" src="https://github.com/user-attachments/assets/0691c28b-0694-4522-a05a-a0342154bc46" />




