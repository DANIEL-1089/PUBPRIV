#include <iostream>
#include <cstdlib>
#include <ctime>
#include <wchar.h>
#include <Windows.h>
#include <algorithm>
#include <vector>
#include <string>
#include <string.h>
#include <stdlib.h>
#include <cstring>
#include <conio.h>
#include <iomanip>
#include <process.h>



using namespace std;
class A {
private:
    int privdataA;
protected:
    int protdataA;
public:
    int pubdataA;
};
class B : public A {
public:
    void funct() {
        int a;
        a = protdataA;
        a = pubdataA;
    }
};
class C : private A {
public:
    void funct() {
        int a;
        a = protdataA;
        a = pubdataA;
    }
};


int main()
{
    int a;
    B objB;
    a = objB.pubdataA;
    
    C objC;

    return 0;
}
