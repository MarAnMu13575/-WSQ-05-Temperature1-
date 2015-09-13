# -WSQ-05-Temperature1-

#include <iostream>
using namespace std;
float celsius;
float fahrenheit;

void convertF()
{
	celsius = ((fahrenheit - 32) * 5) / 9;
}
void convertC()
{
	fahrenheit = (((celsius * 9) / 5) + 32);
}

int main()
{
	unsigned short choice;
	cout << "Welcome to the temperature converter.\n";
	cout << "Please type '1' for Celsius to Fahrenheit conversion." << endl;
	cout << "Or, type '2' for Fahrenheit to Celsius conversion." << endl;
	cin >> choice;

	switch (choice)
{
	case 1:

	cout << "Please enter your temperature in Celsius.\n";

	cin >> celsius;
	convertC();

	cout << "\n";
	cout << "Computing...\n\n";
	cout << "The temperature in Fahrenheit is " << fahrenheit << ".\n";
	if (fahrenheit>221) {
		cout<< "The water is boiling"<<endl;
	}
	if (fahrenheit<32) {
		std::cout << "The water is freez" << std::endl;

	}
	cout << "Press any key to terminate the program." << endl;
	cout << endl;
	break;

	case 2:

	cout << "Please enter your temperature in Fahrenheit.\n";

	cin >> fahrenheit;
	convertF();

	cout << "\n";
	cout << "Computing...\n\n";
	cout << "The temperature in Celsius is " << celsius << ".\n";
	if  (	celsius >100) {
		cout<<"The water is heated"<< endl;
	}
	   if  (celsius<0){
		std::cout<<"The water is freezing"<< std::endl;
	}
	cout << "Press any key to terminate the program." << endl;
	cout << endl;
	break;

	default:

	cout << "That is not an option!" << endl;
	cout << "Please close the program and try again." << endl;
	break;

}

	return 0;
}
