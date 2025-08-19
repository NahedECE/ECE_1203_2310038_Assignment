----------
## *Assignment No : 03*

## *Assignment Name : Constructors, Friend Functions, Classes & Inheritance.*

## **Submission Date : 20th June 2025**

----------
# *Constructor*
-----------
## *Example 1 :*
## *Code :*
```C++
# include<bits/stdc++.h>
using namespace std;
class Cars{
    string companyName;
    string modelName;
    string fuelType;
    float mileage;
    double price;
public:
    Cars(){
        companyName = "Toyota";
    }

    Cars(string modelName, string fuelType, float mileage, double price){
        this -> modelName = modelName;
        this -> fuelType = fuelType;
        this -> mileage = mileage;
        this -> price = price;
    }

    void getData(){
        cout << "Company Name : " << companyName << endl
             << "Model Name : " << modelName << endl
             << "Fuel Type : " << fuelType << endl
             << "Mileage : " << mileage << endl
             << " Price : " << price << endl << endl;
    }

};

int main(){
    
    Cars car1, car2("Fortuner", "Diesel", 10 , 350000);
    car1.getData();
    car2.getData();
    return 0;
}
```

## *Output :*
<p align="center">


![image](https://github.com/user-attachments/assets/e31489a8-39d8-4712-9f7c-27c557925aef)



</p>



--------
## *Example 2 :*
## *Code :*
```C
# include<bits/stdc++.h>
using namespace std;
class Cars{
    string companyName;
    string modelName;
    string fuelType;
    float mileage;
    double price;
public:

    Cars(){
        companyName = "Toyota";
    }
    Cars(string modelName, string fuelType, float mileage, double price){
        this -> modelName = modelName;
        this -> fuelType = fuelType;
        this -> mileage = mileage;
        this -> price = price;
    }

    void setData(string companyName,string modelName, string fuelType, float mileage, double price){
        this -> companyName = companyName;
        this -> modelName = modelName;
        this -> fuelType = fuelType;
        this -> mileage = mileage;
        this -> price = price;
    }


    void getData(){
        cout << "Company Name : " << companyName << endl
             << "Model Name : " << modelName << endl
             << "Fuel Type : " << fuelType << endl
             << "Mileage : " << mileage << endl
             << "Price : " << price << endl << endl;
    }

};

int main(){
    Cars car1, car2("Fortuner", "Diesel", 10 , 350000);
    car1.setData("TOYOTA", "Atlis", "Diesel", 12, 400000);
    car1.getData();
    car2.getData();
    return 0;
}

```

## *Output :*
<p align="center">


![image](https://github.com/user-attachments/assets/ee4ef6aa-c52d-44a2-af3a-c312e7fe15f2)



</p>



--------

## *Example 3 :*
## *Code :*
```C
# include<bits/stdc++.h>
using namespace std;
class Cars{
    string companyName;
    string modelName;
    string fuelType;
    float mileage;
    double price;
public:
    Cars(){
        cout << "Default Constructor is invoked!" << endl;
    }


    Cars(string companyName,string modelName, string fuelType, float mileage, double price){
        cout << "Parameterised Constructor is invoked!" << endl;
        this-> companyName = companyName;
        this -> modelName = modelName;
        this -> fuelType = fuelType;
        this -> mileage = mileage;
        this -> price = price;
    }

    Cars(const Cars &obj){
        cout << "Copy Constructor is invoked!" << endl;
        this -> companyName = obj.companyName;
        this -> modelName = obj.modelName;
        this -> fuelType = obj.fuelType;
        this -> mileage = obj.mileage;
        this -> price = obj.price;
    }

    void setData(string companyName,string modelName, string fuelType, float mileage, double price){
        this -> companyName = companyName;
        this -> modelName = modelName;
        this -> fuelType = fuelType;
        this -> mileage = mileage;
        this -> price = price;
    }

    void getData(){
        cout << "Company Name : " << companyName << endl
             << "Model Name : " << modelName << endl
             << "Fuel Type : " << fuelType << endl
             << "Mileage : " << mileage << endl
             << "Price : " << price << endl << endl;
    }

};

int main(){

    Cars car1, car2("Toyota","Fortuner", "Diesel", 10 , 350000);
    car1.setData("TOYOTA", "Atlis", "Diesel", 12, 400000);
    car1.getData();
    car2.getData();

    //Cars car3(car1); // This will also work

    Cars car3 = car1;
    car3.getData();
    return 0;
}


```

## *Output :*
<p align="center">


![image](https://github.com/user-attachments/assets/3b57040d-104c-44b0-82cf-3a6285034b91)




</p>



--------

# *Accessibility in Inheritance*

---------

## *A chart is provided below on Accessibility in Inheritance from different classes -*

## *In public mode :*
| *Access / Member origin* | *private* | *protected* | *public* |
| ------------------------ | :-------: | :---------: | :------: |
| *From own class*         |   *yes*   |    *yes*    |   *yes*  |
| *From derived class*     |    *no*   |    *yes*    |   *yes*  |
| *From 2nd derived class* |    *no*   |    *yes*    |   *yes*  |

-------

## *In protected mode :*

| *Access / Member origin* | *private* | *protected* | *public* |
| ------------------------ | :-------: | :---------: | :------: |
| *From own class*         |   *yes*   |    *yes*    |   *yes*  |
| *From derived class*     |    *no*   |    *yes*    |   *yes*  |
| *From 2nd derived class* |    *no*   |    *yes*    |   *yes*  |

---------

## *In private mode :*

| *Access / Member origin* | *private* | *protected* | *public* |
| ------------------------ | :-------: | :---------: | :------: |
| *From own class*         |   *yes*   |    *yes*    |   *yes*  |
| *From derived class*     |    *no*   |    *yes*    |   *yes*  |
| *From 2nd derived class* |    *no*   |     *no*    |   *no*   |

---------

# *Checking the chart's validity with the help of code :*

--------

## *Example code of Inheritance in public mode :*
## *Code :*
```C
# include<bits/stdc++.h>
using namespace std;
class BaseClass{
    string privateBaseClassVariable = "Hello, I belong to Base Class and I am a private variable";
public :
    string publicBaseClassVariable = "Hello, I belong to Base Class and I am a public variable";
protected :
    string protectedBaseClassVariable = "Hello, I belong to Base Class and I am a protected variable";
public:
    void canItAccessBaseClass(){
        cout << "Base Class is Acessing it's own variables below :" << endl;
        cout << privateBaseClassVariable << endl
             << publicBaseClassVariable << endl
             << protectedBaseClassVariable << endl << endl;
    }
};

class ChildClass1 : public BaseClass{
public:
    void ChildClass1IsAcessing(){
        cout << "ChildClass1 is Acessing BaseClass's variables below :" << endl;
        cout << privateBaseClassVariable << endl
             << publicBaseClassVariable << endl
             << protectedBaseClassVariable << endl << endl;
    }
};

class ChildClass2 : public ChildClass1{
public:
    void ChildClass2IsAcessing(){
        cout << "ChildClass2 is Acessing BaseClass's variables below :" << endl;
        cout << privateBaseClassVariable << endl
             << publicBaseClassVariable << endl
             << protectedBaseClassVariable << endl << endl;
    }
};

int main(){
    
    ChildClass1 ch1;
    ch1.ChildClass1IsAcessing();
    ChildClass2 ch2;
    ch2.ChildClass2IsAcessing();
    return 0;
}
```

## *Output :*
<p align="center">


![image](https://github.com/user-attachments/assets/b83df6fa-d52d-4817-a14f-af64c96f81e7)




</p>

## *Errors and Warnings :*
*BaseClass's only private variables are not being able to access from ChildClass1 and ChildClass2. Rest of them are accessible from both classes.*
---------
--------


## *Example code of Inheritance in protected mode :*
## *Code :*
```C
# include<bits/stdc++.h>
using namespace std;
class BaseClass{
    string privateBaseClassVariable = "Hello, I belong to Base Class and I am a private variable";
public :
    string publicBaseClassVariable = "Hello, I belong to Base Class and I am a public variable";
protected :
    string protectedBaseClassVariable = "Hello, I belong to Base Class and I am a protected variable";
public:
    void canItAccessBaseClass(){
        cout << "Base Class is Acessing it's own variables below :" << endl;
        cout << privateBaseClassVariable << endl
             << publicBaseClassVariable << endl
             << protectedBaseClassVariable << endl << endl;
    }
};

class ChildClass1 : protected BaseClass{
public:
    void ChildClass1IsAcessing(){
        cout << "ChildClass1 is Acessing BaseClass's variables below :" << endl;
        cout << privateBaseClassVariable << endl
             << publicBaseClassVariable << endl
             << protectedBaseClassVariable << endl << endl;
    }
};

class ChildClass2 : protected ChildClass1{
public:
    void ChildClass2IsAcessing(){
        cout << "ChildClass2 is Acessing BaseClass's variables below :" << endl;
        cout << privateBaseClassVariable << endl
             << publicBaseClassVariable << endl
             << protectedBaseClassVariable << endl << endl;
    }
};

int main(){
    optimize();

    ChildClass1 ch1;
    ch1.ChildClass1IsAcessing();
    ChildClass2 ch2;
    ch2.ChildClass2IsAcessing();
    return 0;
}
```

## *Output :*
<p align="center">


![image](https://github.com/user-attachments/assets/245a9aa0-37e3-4288-a8fc-ebcb7b947799)



</p>

## *Errors and Warnings :*
*BaseClass's only private variables are not being able to access from ChildClass1 and ChildClass2. Rest of them are accessible from both classes.*
---------
--------


## *Example code of Inheritance in private mode :*
## *Code :*
```C
# include<bits/stdc++.h>
using namespace std;
class BaseClass{
    string privateBaseClassVariable = "Hello, I belong to Base Class and I am a private variable";
public :
    string publicBaseClassVariable = "Hello, I belong to Base Class and I am a public variable";
protected :
    string protectedBaseClassVariable = "Hello, I belong to Base Class and I am a protected variable";
public:
    void canItAccessBaseClass(){
        cout << "Base Class is Acessing it's own variables below :" << endl;
        cout << privateBaseClassVariable << endl
             << publicBaseClassVariable << endl
             << protectedBaseClassVariable << endl << endl;
    }
};

class ChildClass1 : private BaseClass{
public:
    void ChildClass1IsAcessing(){
        cout << "ChildClass1 is Acessing BaseClass's variables below :" << endl;
        cout << privateBaseClassVariable << endl
             << publicBaseClassVariable << endl
             << protectedBaseClassVariable << endl << endl;
    }
};

class ChildClass2 : private ChildClass1{
public:
    void ChildClass2IsAcessing(){
        cout << "ChildClass2 is Acessing BaseClass's variables below :" << endl;
        cout << privateBaseClassVariable << endl
             << publicBaseClassVariable << endl
             << protectedBaseClassVariable << endl << endl;
    }
};

int main(){
    optimize();

    ChildClass1 ch1;
    ch1.ChildClass1IsAcessing();
    ChildClass2 ch2;
    ch2.ChildClass2IsAcessing();
    return 0;
}
```

## *Output :*
<p align="center">


![image](https://github.com/user-attachments/assets/20f83137-bdd9-45c5-b244-232ffd81a476)




</p>

## *Errors and Warnings :*
*ChildClass1 can not access private data member and ChildClass2 can not access any data member from BaseClass.*
--------
-------

# *Friend Function & Class*

--------

## *Friend Function :*

## *Code :*
```C
# include<bits/stdc++.h>
using namespace std;
double areaCalculator(double, double);

class Rectange{
    double length;
    double width;
    double area;
public:
    Rectange(double length, double width){
        this -> length = length;
        this -> width = width; 
    }

    // Friend Declaration
    friend double areaCalculator(double, double);

    void getArea(){
        area = areaCalculator(length,width);
        cout << "The area of the Rectangle with length " << length << " and width " << width << " is : " << area << endl << endl;
    }
};

double areaCalculator(double length, double width){
    return length*width;
}

int main(){
    optimize();
    Rectange r1(2,3);
    r1.getArea();      
    return 0;
}
```

## *Output :*
<p align="center">


![image](https://github.com/user-attachments/assets/18e62d3c-bb01-468b-923d-d4c2fe9f8589)




</p>


--------


## *Friend Class :*

## *Code :*
```C
# include<bits/stdc++.h>
using namespace std;
class AreaCalculator;

class Rectangle{
    double length;
    double width;
    double area;
public:
    Rectangle(double length, double width){
        this -> length = length;
        this -> width = width; 
    }

    // Friend Declaration
    friend class AreaCalculator;

};

// Friend Class
class AreaCalculator{
public:
    void calculate(Rectangle &obj){
        cout << "The area of the Rectangle with length " << obj.length << " and width " << obj.width << " is : " << obj.length * obj.width << endl << endl;
    }
};

int main(){
    optimize();
    Rectangle r(2,3);
    AreaCalculator obj;
    obj.calculate(r);
    return 0;
}
```

## *Output :*
<p align="center">


![image](https://github.com/user-attachments/assets/0d1abb5a-9a46-4a09-8f41-708ce80f0289)




</p>


--------

