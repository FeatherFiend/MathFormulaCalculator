# MathFormulaCalculator
Math formula repository

Alex: Create an easy-to-use "formula sheet"
Note: "\" is used to override default formatting (ex: to dereference a pointer -> \*p is necessary)

#include<vector>
#include<set>
#include<iostream>
#include<string>
#include<complex>
#include<cmath>
  
using namespace std;

//Convention: independent variables come first

//Function prototypes
void prompt();
bool valid_input(int numInput);
double pythagorean_formula(double a = 0, double b = 0, double c = 0);
double circle_area_formula(double r = 0, double c = 0);
double circumference_formula(double r = 0, double c = 0);


//Classes
struct ArgumentError{};

//Globals
constexpr double PI = 3.14159265359;

int main()
{
	set<string> formulaList;
	
	cout<<"Formula: ";
	string formulaName;
	getline(cin, formulaName);
	
	return 0;
}

bool valid_input(iterator start, iterator end)
{
	int counter = 0;
	for(iterator p = start; p != end; p++){
		if(\*p == 0)
      		counter++;
  	}
	if(counter != 1)
		return false;
		
	return true;
}

double pythagorean_formula(double a = 0, double b = 0, double c = 0)
{
	vector<double> input {a, b, c};
	if(!valid_input(input.begin(), input.end()) throw ArgumentError{};
	
	if(c != 0)
		return sqrt(pow(c, 2) - pow(b, 2) - pow(c, 2))	//either a^2 or b^2 == 0 
	else
		return sqrt(pow(a, 2) + pow(b, 2))
}

double circle_area_formula(double r = 0, double c = 0)
{
	vector<double> input {r, c};
	if(!valid_input(input.begin(), input.end()) throw ArgumentError{};
	
	if(c == 0)
		return PI * pow(r, 2);
	else
		return sqrt(c / PI);
}

double circumference_formula(double r = 0, double c = 0)
{
	vector<double> input {r, c};
	if(!valid_input(input.begin(), input.end()) throw ArgumentError{};
	
	if(c == 0)
		return 2 * PI * r;
	else
		return C / (2 * PI);
}
