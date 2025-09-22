# Lab-Decision-and-Switch-Statements
Decision and switch statements lab

## Challenges
The challenges I faced while coding this assignment were:
1. Remembering to use double when creating a place for numbers to be inputted. My mind auto types int when I'm coding.
2. Using static_cast to make sure that the input was read in the enum class rather than just using switch with the int that's inputted.
3. Remembering to put 'break;' after each case and making sure that I followed all proper syntac when calling from the operation enum.

## Code:
```#include <string>
#include <iostream>

using namespace std;

enum class Operation {
    Add = 1,
    Subtract,
    Multiply,
    Divide,
    Quit
};

int main()
{
	while (true) {

	int opChoice;
	cout << "1. Add\n2. Subtract\n3. Multiply\n4. Divide\n5. Quit" << endl; //Menu for the user to choose from
	cin >> opChoice;
	Operation operation = static_cast<Operation>(opChoice); //Casting the user input to the enum class

	switch (operation) {
	case Operation::Add: //Takes the add operation from the enum class
		cout << "Please input two numbers to add: ";
		{
			double a, b;
			cin >> a >> b;
			cout << "The sum is " << (a + b) << endl;
		}
		break;

	case Operation::Subtract: //Takes the subtract operation from the enum class
		cout << "Please input two numbers to subtract: ";
		{
			double a, b;
			cin >> a >> b;
			cout << "The difference is " << (a - b) << endl;
		}
		break;

	case Operation::Multiply: //Takes the multiply operation from the enum class
		cout << "Please input two numbers to multiply: ";
		{
			double a, b;
			cin >> a >> b;
			cout << "The product is " << (a * b) << endl;
		}

		break;

	case Operation::Divide: //Takes the divide operation from the enum class
		cout << "Please input two numbers to divide: ";
		{
			double a, b;
			cin >> a >> b;
			if (b == 0) {
				cout << "Error: Cannot Divide by zero" << endl;
			}
			else {
				cout << "The quotient is " << (a / b) << endl;
			}
		}
			break;

	case Operation::Quit: //Takes the quit operation from the enum class
		cout << "Quitting the program." << endl;
		return 0;
		break;

	default:
		cout << "Invalid operation selected." << endl;
	}
		}
	}
```

## Video Link
