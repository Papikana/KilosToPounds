# KilosToPounds
Repository
// Lab 6 kiloConverter.cpp 
 // This menu-driven program lets the user convert 
 // pounds to kilograms and kilograms to pounds.
 // Papikana
 #include <iostream>
#pragma unmanaged
#pragma managed
 using namespace std;

 // Function prototypes
 void displayMenu();
 int getChoice(int, int);// WRITE PROTOTYPES FOR THE displayMenu, getChoice,
 double kilosToPounds();
 double poundsToKilos();// kilosToPounds and poundsToKilos FUNCTIONS HERE.

 /*****     main     *****/
 int main()
 {
	 int choice;
	 do {
		 displayMenu();
		 choice = getChoice(1, 3);
		 if (choice == 1) {
			 cout << "Weight: " << kilosToPounds() << endl << endl;
		 }
		 else if (choice == 2)
			 cout << "Weight: " << poundsToKilos() << endl << endl;
	 } while (choice != 3);	
		    return 0;
	 }

 /*****     displayMenu     *****/
 void displayMenu() {
	 cout << "Please choose an option. [1]Kilos>>Pounds [2]Pounds>>Kilos [3]Exit." << endl;
 }

 /*****     getChoice     *****/
 int getChoice(int min, int max)
 {
	 int input;
	 cin >> input;
	 if (isdigit(input)) {
		 while ((input < min || input > max))
		 {
			 cout << "Invalid input. Enter an integer between " << min << " and " << max << ": ";
			 cin >> input;
		 }
	 }
	 else
		 cout << "Invalid input. Enter an integer between " << min << " and " << max << ": ";
	 return input;
 } 

 /*****     kilosToPounds     *****/
 double kilosToPounds() 
 {
	 double weight, kilos;
	cout << "Please enter kilos: ";
	 cin >> kilos;
	 weight = kilos * 2.1;
		return weight;
 
 }
 /*****    poundsToKilos     *****/
 double poundsToKilos()
 {
	 double weight, pounds;
	 cout << "Please enter pounds: ";
	 cin >> pounds;
	 weight = pounds / 2.1;
	 return weight;
 }
