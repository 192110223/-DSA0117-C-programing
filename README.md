
#include <iostream>
using namespace std;
class Rectangle {
public:
    int length, breadth;
    Rectangle(int a) {
        length = a;
        breadth = a;
    }
    void area() {
        cout << "Area of Rectangle: " << length * breadth << endl;
    }
};
class Box {
public:
    int length, width, height;
    Box() {
        length = width = height = 1;
    }
    Box(int a) {
        length = width = height = a;
    }
    Box(int l, int w, int h) {
        length = l;
        width = w;
        height = h;
    }
    void volume() {
        cout << "Volume of Box: " << length * width * height << endl;
    }
};
int main() {
    Rectangle r(4);
    r.area();
    Box b1;
    Box b2(3);
    Box b3(2, 3, 4);
    b1.volume();
    b2.volume();
    b3.volume();
    return 0;
}
