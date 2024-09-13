# Exp-13--Function--Operator-Overloading
# AIM
To learn fucntion overloading in c++.

# Software Used

VS Code

# Problem Statement

1.) Write a c++ program to do function overloading.

2.) Write a c++ program to do operator overloading.

# Theory

Function overloading is a feature of object-oriented programming where two or more functions can have the same name but different parameters. When a function name is overloaded with different jobs it is called Function Overloading. In Function Overloading “Function” name should be the same and the arguments should be different. Function overloading can be considered as an example of a polymorphism feature in C++.

Operator overloading is a compile-time polymorphism. It is an idea of giving special meaning to an existing operator in C++ without changing its original meaning.

In this article, we will further discuss about operator overloading in C++ with examples and see which operators we can or cannot overload in C++.

# Problem Codes

```javascript


//FUNCTION OVERLOADING
#include<iostream>
using namespace std;
int add(int a, int b){
    return a+b ;
}
float add(float a, float b)
{
    return a+b;

}
int add(int a, int b , int c){
    return a+b+c;
}
int main() {
    cout<<"Addition of 2 integers: "<<add(3,4)<< endl;
    cout<< "Addition of 2 floats: "<<add(3.5f, 4.5f)<<endl;
    cout<< "Addition of 3 integers: "<< add(1,2,3)<<endl;
    return 0;
    }


//OPERATOR OVERLOADING
#include<iostream>
using namespace std;
class Complex {
    private:
    float real;
    float imag;
     
     public:
     Complex(float r =0 , float i = 0)
     
     {
        real = r;
        imag =i;
     }
Complex operator + (const Complex &obj)
{
    Complex temp;
    temp.real = real + obj.real;
    temp.imag = imag + obj.imag;
    return temp;
}
void display()const {
    cout<< real<<" + "<< imag<< "i"<<endl;
}
};
int main() {
    Complex c1(3.5,2.5);
    Complex c2(1.6,3.7);
    Complex c3 = c1 +c2;
   
    cout << "First complex number: ";
    c1.display();
    cout << "Second complex number: ";
    c2.display();
    cout << "Sum of complex numbers: ";
    c3.display();
    return 0;

}

```

# Output
## Function Overloading
![Exp 13 Function Overloading](https://github.com/user-attachments/assets/9a5016cd-2843-4917-b32e-3fe1294fcdcf)

## Operator Overloading
![Exp 13 Operator Overloading](https://github.com/user-attachments/assets/507c08a2-9329-41e4-8e93-4e8f9c5b568d)

# Conclusion
We learnt to do function and operator overloading.
