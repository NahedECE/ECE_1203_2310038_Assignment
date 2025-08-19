## **Assignment No : 02**

## **Assignment Name : Output of constructor codes**

## **Submission Date : May 19, 2025**

## Default Constructor:
```C
#include<iostream>
using namespace std;

class Car{
    int x, y;
    public:
    Car(){
        cout << "Here is the car";
    }
};

int main()
{
    Car car1;
}

```

## **Output :** 
<img width="1261" height="214" alt="image" src="https://github.com/user-attachments/assets/ac7fe10c-997c-4bfb-8c50-78c0b126f10f" />


## Parameterized Constructor:
```C
#include<iostream>
using namespace std;

class Car{
    int price;
    public:
    Car(int value){
        price = value;
        cout << "Here is the car" << endl;
        cout << "Parameterized constructor";
    }
};

int main()
{
    Car car1(6500);
}


```

## **Output :** 
<img width="1026" height="205" alt="image" src="https://github.com/user-attachments/assets/0dd0aa1e-91d1-4e75-93ed-9c1e3983990d" />



## Parameterized Constructor:
```C
#include<iostream>
using namespace std;

class Car{
    public:
    int year;
    string brand;
    string model;

    Car(string x, string y, int z){
        brand = x;
        model = y;
        year = z;
    }
};

int main()
{
    Car car1("Toyota", "MO4860MI38", 2022);

    cout << "The car is: " << car1.brand << " " << car1.model << "," << car1.year << endl;
}


```

## **Output :** 
<img width="1255" height="204" alt="image" src="https://github.com/user-attachments/assets/3ead9d61-bf63-477e-a26b-30d4d37ba5b9" />


## Parameterized Constructor:
```C
#include<iostream>
using namespace std;

class Car{
    public:
    int year;
    string brand;
    string model;

    Car(string x, string y, int z);
};

Car::Car(string x, string y, int z){
        brand = x;
        model = y;
        year = z;
    }
  
int main()
{
    Car car1("Ford", "MO3150SI", 2020);

    cout << "The car is: " << car1.brand << " " << car1.model << "," << car1.year << endl;
}

```

## **Output :** 
<img width="1247" height="224" alt="image" src="https://github.com/user-attachments/assets/2973a5b9-5d4d-440a-9ab1-2bbb60420806" />


## Constructor:
```C
#include<iostream>
using namespace std;

class Cars{
    string company;
    string model;
    string fuel;
    int year;
    float mileage;
    double price;

    public:
    Cars() {}
    void setData(string carname, string modlename, string fuelname, int a, float ml,double pr)
    {
        company = carname;
        model = modlename;
        fuel = fuelname;
        year = a;
        mileage = ml; 
        price = pr;
    }

    void DisplayData()
    {
        cout << "Company: " << company << "\n";
        cout << "Model: " << model << "\n";
        cout << "Fuel: " << fuel << "\n";
        cout << "Mileage: " << mileage << "\n";
        cout << "Year: " << year << "\n";
        cout << "Price: " << price << "\n";
    }
};

  
int main()
{
    Cars car1;

    car1.DisplayData();
}
```

## **Output :** 
<img width="1252" height="331" alt="image" src="https://github.com/user-attachments/assets/cfb7a801-67e9-4f1f-8538-1831b5fae3fa" />


## Constructor:
```C
#include<iostream>
using namespace std;

class Cars{
    string company;
    string model;
    string fuel;
    int year;
    float mileage;
    double price;

    public:
    Cars() { company = "Rolls Royce";}
    Cars(string modname, string fname, int y, float mile,double p)
    {
        model = modname;
        fuel = fname;
        mileage = mile;
        year = y;
        price = p;
    }

    void DisplayData()
    {
        cout << "Company: " << company << "\n";
        cout << "Model: " << model << "\n";
        cout << "Fuel: " << fuel << "\n";
        cout << "Mileage: " << mileage << "\n";
        cout << "Year: " << year << "\n";
        cout << "Price: " << price << "\n";
    }
};

  
int main()
{
    Cars car1, car2("NAMOSI","M48S38OIF60", 2022, 48.60, 31538.48);

    car1.DisplayData();
    car2.DisplayData();
}
```

## **Output :** 
<img width="1256" height="543" alt="image" src="https://github.com/user-attachments/assets/3c9baf79-cc8f-455f-be82-c27fbcf31220" />


## Constructor:
```C
#include<iostream>
using namespace std;

class Cars{
    string company;
    string model;
    string fuel;
    float mileage;
    double price;

    public:
    Cars() { company = "Rolls Royce";}
    Cars(string cname, string mname, string fname, float mile,double p)
    {
        company = cname;
        model = mname;
        fuel = fname;
        mileage = mile;
        price = p;
    }

    void setData(string carname, string modname, string flname, float ml,double prc)
    {
        company = carname;
        model = modname;
        fuel = flname;
        mileage = ml;
        price = prc;
    }
    void DisplayData()
    {
        cout << "Company: " << company << "\n";
        cout << "Model: " << model << "\n";
        cout << "Fuel: " << fuel << "\n";
        cout << "Mileage: " << mileage << "\n";
        cout << "Price: " << price << "\n";
    }
};

  
int main()
{
    Cars car1, car2("NAMOSIM", "MO48SI38MI60","PosMI", 46.10, 23315048);
    car1.setData("Ford","MO4860", "38SI", 48.38, 3214860);
    car1.DisplayData();
    car2.DisplayData();
}
```

## **Output :** 
<img width="1276" height="454" alt="image" src="https://github.com/user-attachments/assets/2f054cc4-f5de-4c6c-93ea-0d79e45d9a5f" />

![image](https://github.com/user-attachments/assets/64298c85-15ed-4d14-9f0a-6c10c50bb92f)

