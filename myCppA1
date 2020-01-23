/*Written by Somaly Ngov
  Last Updated: 09/17/2019
  */
#include <iostream>
#include <string>
#include <fstream>

//prototype
int linearSearch(char*, int, int);
int binarySearch(int*, int, int, int);

int main()
{

	std::ifstream inFile("Input.txt");
	int value;
	int s; // holding variable
	int lenght = 18;
	int l = 17;
	char inChar;

	int num[18]{};
	char let[17]{};

	//code to exit out of the program, if Input.txt doesn't exist.
	if (!inFile) {
		std::cout << "Cannot open file. \n";
		return 1;
	}

	//The unsorted list of integers
	for (int i = 0; i < 18; i++) {
		inFile >> num[i];
	}
	std::cout << "The unsorted list of integers:" << std::endl;
	for (int i = 0; i < 18; i++) {
		/* This statement would be executed
		* repeatedly until the condition
		* i<18 returns false.
		*/
		std::cout << num[i] << " ";
	}

	//The unsorted list of characters
	for (int i = 0; i < 17; i++) {
		inFile >> let[i];
	}
	std::cout << " " << std::endl;
	std::cout << " " << std::endl;
	std::cout << "The unsorted list of characters:" << std::endl;
	for (int i = 0; i < 17; i++) {
		/* This statement would be executed
	   * repeatedly until the condition
	   * i<17 returns false.
	   */
		std::cout << let[i] << " ";
	}

	//The sorted list of integers in descending order
	std::cout << " " << std::endl;
	std::cout << " " << std::endl;
	std::cout << "The sorted list of integers in descending order:" << std::endl;
	
	
	for (int j = 0; j < lenght; j++) {
		for (int i = 0; i < lenght-1; i++) {
			if (num[i] < num[i + 1]) {
				s = num[i + 1];
				num[i + 1] = num[i];
				num[i] = s;
			}
		}

	}

	
	for (int i = 0; i < 18; i++) {
		std::cout << num[i] << " ";
	}

	
	//The sorted list of characters in ascending order
	std::cout << " " << std::endl;
	std::cout << " " << std::endl;
	std::cout << "The sorted list of characters in ascending order:" << std::endl;
	for (char j = l - 1; j >= 0; j++) {
		for (char i = 0; i < l; i++) {
			if (let[i] < let[i - 1]) {
				s = let[i - 1];
				let[i - 1] = let[i];
				let[i] = s;// swap elements
			}
		}
	}
	for (int i = 0; i <17; i++) {
		std::cout << let[i] << " ";
	}


	//use binary search to search for the location of integer that user input
	std::cout << " " << std::endl;
	std::cout << " " << std::endl;
	std::cout << "Enter the number that you want to search:";
	std::cin >> value;

	int n = sizeof(num) / sizeof(num[0]);
	int result = binarySearch(num, 0, n-1, value);
	if (result == -1)
		std::cout << "Element is not present in the array";
	else
	    std::cout << "Element is present at index " << result;

	//use linear search to search for the location of the character.
	std::cout << " " << std::endl;
	std::cout << " " << std::endl;
	std::cout << "Enter the character that you want to search:";
	std::cin >> inChar;
	int o = sizeof(let) / sizeof(let[0]);


	int index = linearSearch(let, o, inChar);
	if (index == -1)
		std::cout << "Element is not present in the array";
	else
		std::cout << "Element found at position " << index;
	

	inFile.close();
	return 0;
}

//binary search
int binarySearch(int *num, int l, int r, int x)
{
	while (l <= r) {
		int m = l + (r - l) / 2;

		// Check if x is present at mid 
		if (num[m] == x)
			return m;

		// If x greater, ignore left half 
		if (num[m] > x)
			l = m + 1;

		// If x is smaller, ignore right half 
		else
			r = m - 1;
	}
	return -1;
}
void let(char arr[], int size) {
	for (int i = 0; i < size; i++)
		std::cout << arr[i] << " ";
}

//linear search
int linearSearch(char *let, int n, int x)
{
	int i{};
	for (i = 0; i < n; i++) {
		if (let[i] == x)
			return i;
	}
	return -1;
}

