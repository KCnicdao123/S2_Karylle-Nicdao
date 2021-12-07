# S2_Karylle-Nicdao

#include <iostream>
#include <string>
#include <math.h>

using namespace std;

int main()
{
	string name;
	int userNum, y = 0, fact = 1, x = 0;
	cout << "Please enter you full name:" << endl;
	getline (cin, name);
	cout << "Enter a number to find its factorial, table, and exponent power until 10:" << endl;
	cin >> userNum;
	while (cin.fail()) {
		cin.clear();
		cin.ignore(1000, '\n');
		cout << "Invalid input. Please enter a number:" << endl;
		cin >> userNum;
	}
	while (y < userNum) {
		y++;
		fact *= y;
	}
	cout << "\nThe factorial of " << userNum << " is: " << fact << endl;
	cout << "\nThe table of " << userNum << " until 10 is:" << endl;
	do {
		x++;
		cout << userNum << " x " << x << " = " << userNum * x << endl;
	} while (x < 10);
	cout << endl;
	for (int exp = 0; exp <= 10; exp++) {
		cout << userNum << " to the power of " << exp << " is " << pow(userNum, exp) << endl;
	}
}
