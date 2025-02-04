#include <iostream>

using namespace std;

class array 

{

private:

 int arr[5]; 

public:

 void initializearray()

 {

 for (int i = 0; i < 5; i++) 

 {

 arr[i] = i * 10; 

 }

 }

 void displayarray() {

 cout << "One-dimensional array: ";

 for (int i = 0; i < 5; i++)

 {

 cout << arr[i] << " ";

 }

 cout << endl;

 }

};

main() 

{

 array handler;

 handler. initializearray();

 handler.displayarray(); 

}
