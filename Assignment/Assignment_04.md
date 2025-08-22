## **Assignment No : 04**

## **Assignment Name : 10 Keywords with examples**

## **Submission Date : 20 June, 2025**

# 10 C++ Keywords with Examples and Discussion

---

## 1. `signed`


```cpp
#include <iostream>
using namespace std;

int main() {
    signed int a = -5;
    int b = 10; // this is also signed by default
    cout << a << " " << b << endl;
    return 0;
}
```
## Discussion:
Signed is used to declare variables which can have both positive and negative values. By default variables are signed.


## 2. `static`

```cpp
#include <iostream>
using namespace std;

void countCalls() {
    static int count = 0;
    count++;
    cout << "Called " << count << " times\n";
}

int main() {
    countCalls();
    countCalls();
    countCalls();
    return 0;
}
```
## Discussion:
## static make the code to remeber the value. Every time the funtion is called the value of count is remebered, so the value goes up by 1 everytime it is called.
## When static is used in class, The variable is shared by all objects of the class.

## 3. `sizeof`

```cpp
#include <iostream>
using namespace std;

int main() {
   cout << sizeof(int);
}
```

## Discussion:
## By using sizeof(), we can see the size of any object, variable or data types.

## 4. `static_cast`

```cpp
#include <iostream>
using namespace std;

int main() {
double d = 3.5;
int x = static_cast<int>(d); 
}
```

## Discussion:
## static_cast is used to convert between different data types safely.

## 5. `struct`

```cpp
#include <iostream>
using namespace std;

struct Student {
  string name;
  int age;
};

int main() {
   struct Student s1;
}
```

## Discussion:
## struct keyword is used to create structure which is to group different variables together or to create a new data type, which can be used to create new kinds of variables.


## 6. `switch`

```cpp
#include <iostream>
using namespace std;


int main() {
  int day;
  cin >> day;
   switch(day) {
  case 1: cout << "Monday"; break;
case 2: cout << "Tuesday"; break;
}

}
```

## Discussion:
## switch is used to create conditional statements like if else.

## 7. `throw`

```cpp
#include <iostream>
using namespace std;

int main() {
  throw "Error happened!";

}
```

## Discussion:
## throw is used to manually raise or show errors.

## 8. `true`

```cpp
#include <iostream>
using namespace std;

int main() {
   bool b;
b = true;
}
```

## Discussion:
## true is used is boolean variables to say that its value is 1.

## 9. `template`

```cpp
#include <iostream>
using namespace std;

template <typename T>
T add(T a, T b) {
    return a + b;
}

int main() {
    cout << add<int>(3, 4) << endl;
    cout << add<double>(3.5, 2.1) << endl;
    cout << add<string>("Hi ", "there") << endl;
    return 0;
}

```

## Discussion:
## template is used to create a function or class templates for different data types. we can use the same function with different kinds of variables.


## 10. `this`

```cpp
#include <iostream>
using namespace std;

class Student {
private:
    int id;
public:
    void setId(int id) {
        this->id = id;
    }

    void printId() {
        cout << "ID: " << this->id << endl;
    }
};

int main() {
    Student s;
    s.setId(101);
    s.printId();
    return 0;
}


```

## Discussion:
## When we use setters or parameterized constructors, we have to use different names than the members variables but "this" is a special pointer, which points to current object, so same name can be used.


















