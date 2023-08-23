// Serhiy Leonchyk
// Weight Converter Program

/* This Program uses a few functions to be able to
weight in pounds and ounces, to kilograms and grams */

#include <string>
#include <iostream>
#include <iomanip>
#include <cmath> 

using namespace std;

const double GRAMS_IN_POUND = 453.6;
const double GRAMS_IN_OUNCE = 28.3495;

int PromptAndGetInt(string weightType);

double ConvertToGrams(int pounds, int ounces);

void OutputResults(int pounds, int ounces, int grams);

int main() {
int pounds, ounces, grams;
cout << setw(40) << "Welcome to the Weigth Converter!" << endl;
pounds = PromptAndGetInt("Pounds");
ounces = PromptAndGetInt("Ounces");
grams = ConvertToGrams(pounds, ounces);
OutputResults(pounds, ounces, grams);
return 0;
}

int PromptAndGetInt(string weightType)// Outputs the Type of Weight that Needs to be Input

/* Makes Program Simpler Rather than Having 2
Seperate Functions For Pounds and Ounces */
{
int weight;
cout << "Please enter the " << weightType << " as a whole number: ";
cin >> weight;
return weight;
}


double ConvertToGrams(int pounds, int ounces) // Convert Pounds and Ounces to Grams
{
double grams = 0;
grams += GRAMS_IN_POUND * pounds; // Adds the Grams in the Pounds to
the Variable
grams += GRAMS_IN_OUNCE * ounces; // Adds the Grams in the Ounces to
the Variable
return round(grams / 1); // Rounds to the Nearest Whole Gram
}


void OutputResults(int pounds, int ounces, int grams)// Function to Output Table and Numbers
{
int kilograms;
kilograms = grams / 1000;     // Converts Grams to Kilograms
grams = grams % 1000;         // Remaining Grams after
Kilogram Division
if (ounces >= 16)             // If There are more Ounces than 16, Then more Pounds can be made 
{
  pounds += ounces / 16;
  ounces = ounces % 16;
}
cout << endl;                  // Beginning of Output Table
cout << setw(30) << "Weight Conversion Table" << endl;
cout << setw(10) << "Pounds" << setw(10) << "Ounces" << setw(10) << "Kilograms"
<< setw(10) << "Grams" << endl;
cout << setw(8) << pounds << setw(10) << ounces << setw(9) << kilograms <<
setw(12) << grams << endl;     // End of Output Table
}
