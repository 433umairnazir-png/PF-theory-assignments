Programming Fundamentals — Coursework
Name: Umair Hassam Roll No: 028 (SU92-BSSEM-F25-028) Class / Section:
BSSE 2A / SE-2A Subject: Programming Fundamentals (PF) Instructor: Umar Khalil
This repository contains a collection of C++ assignments, a mini project, and MCQ practice for the Programming Fundamentals course.
📑 Table ofContents
 	 Assig nment 1 – Making Decisions (Tasks 1–20)
 	 Assignment 3 – Part 1: Arrays & Functions
 	 Assig nment 3 – Part 2: Arrays, Sorting & Strings
 	 Assignment 3 – Part 3: Arrays & 2D Arrays
 	 Assig nment 3 – 2D Arrays, Overloading & C-Strings
 	 Mini Project: Restaurant Billing System
 	 MCQs – Chapters 2, 3 & 4

Assignment 1 – Making Decisions (Tasks 1–20)


Practice problems covering conditions.
Task 1 – Simple Condition

/

,

-style chains, logical operators, and nested
















Task 2 – Temperature Range Validator

















Task 3 – Larger / Smaller ofTwo Numbers


















Task 4 – Floating Point Comparison

Task 5 – Safe Division


















Task 6 – Logical Operators Practice

















Task 7 – Race Placement (First Runner)




















Task 8 – Shape Area Menu

cpp

#include <iostream> using namespace std; int main() {
int choice;
cout << " 1. Circle\n2. Rectangle\n3. Triangle\n";
cin >> choice;
if ( choice == 1) {
double r;
cout << " you chose circle" << endl;
cout << " enter value of r: ";
cin >> r;
cout << 3. 14159 * r * r;
} else if ( choice == 2) {
double l, w;
cout << " you chose Rectangle" << endl; cout << " enter length and width: "; cin >> l >> w;
cout << l * w;
} else if ( choice == 3) {
double b, h;
cout << " you chose Triangle" << endl;
cout << " enter base and heigt: ";
cin >> b >> h;
cout << 0. 5 * b * h;
}
return 0;
}

Task 9 – Print Alphabet with ASCII Codes













Task 10 – Weight Classiﬁer




















Task 11 – Sales Bonus Calculator

Task 12 – Loan Qualiﬁcation Check



















Task 13 – TV Model Features























Task 14 – Magic Date Checker

















Task 15 – Commission Rate





















Task 16 – Checking Account Fee Calculator


























Task 17 – Subscription Price Menu




















Task 18 – Monthly Plan Cost























Task 19 – Data Package Cost Calculator

Task 20 – Seconds to Days/Hours/Minutes
























Assignment 3 – Part 1: Arrays & Functions
Instructor: Umar Khalil
Problem 1 – Average ofan Array


































Note: In the input loop,

should be

— reading into

is out

ofbounds and never ﬁlls the array correctly.
Problem 2 – Largest and Smallest Values in an Array


#include <iostream>
using namespace std;
int calculateLowest( int arr[] , int size) {
int lowest = arr[0] ;
for ( int i = 1; i < size; i++) {
if ( arr[i] < lowest) {
lowest = arr[i] ;
}
}
return lowest;
}
int calculateHighest( int arr[] , int size) {
int highest = arr[0] ;
for ( int i = 1; i < size; i++) {
if ( arr[i] > highest) {
highest = arr[i] ;
}
}
return highest;
}
int main() {
int n;
cin >> n;
int arr[n] ;
for ( int i = 0; i < n; i++) {
cin >> arr[i] ;
}
cout << " Lowest Score: " << calculateLowest( arr, n) << endl; cout << " Highest Score: " << calculateHighest( arr, n) ; return 0;
}

Problem 3 – Custom Power Function

























Problem 4 – Voltage Calculator




















Problem 5 – Cricket Team Initial Finder



























Problem 6 – Word Length Calculator



























Assignment 3 – Part 2: Arrays, Sorting & Strings
Instructor: Umar Khalil

Problem 1 – 2nd Highest and 2nd Lowest Values in an Array

cpp

#include <iostream>
using namespace std;
int calculate2Low( int a[] , int size) {
for ( int i = 0; i < size - 1; i++) {
for ( int j = i + 1; j < size; j++) {
if ( a[i] > a[j] ) { int num = a[i] ; a[i] = a[j] ; a[j] = num;
}
}
}
return a[1] ;
}
int calculate2High( int a[] , int size) {
return a[size - 2] ;
}
int main() {
int n;
cout << " enter number of student: ";
cin >> n;
int a[n] ;
cout << " enter score: ";
for ( int i = 0; i < n; i++) {
cin >> a[i] ;
}
cout << " 2nd lowest " << calculate2Low( a, n) << endl;
cout << " 2nd highest " << calculate2High( a, n) ;
}

Problem 2 – Sumofan Array


























Problem 3 – Temperature Converter (Celsius → Fahrenheit)




















Problem 4 – Leap Year Checker





















Problem 5 – Vowel Counter
























Problem 6 – Alphabetical Sorter (Bubble Sort on Chars)

































 
Assignment 3 – Part 3: Arrays & 2D Arrays
Roll No: SU92-BSSEM-F25-003
Problem 1 – Count Even and Odd Numbers in an Array


#include <iostream>
using namespace std;
int countEvenNumbers( int arr[] , int size) {
int count = 0;
for ( int i = 0; i < size; i++) {
if ( arr[i] % 2 == 0) {
count++;
}
}
return count;
}
int countOddNumbers( int arr[] , int size) {
int count = 0;
for ( int i = 0; i < size; i++) {
if ( arr[i] % 2 ! = 0) {
count++;
}
}
return count;
}
int main() {
int N;
cout << " Enter Size of Array: ";
cin >> N;
int numbers[N] ;
for ( int i = 0; i < N; i++) {
cout << " Enter value in index " << i << ": ";
cin >> numbers[i] ;
}
int even = countEvenNumbers( numbers, N) ;
int odd = countOddNumbers( numbers, N) ;
cout << " Number of Even Numbers in Array: " << even << endl; cout << " Number of Odd Numbers in Array: " << odd << endl; return 0;
}

Problem 2 – Display a 2D Array































Problem 3 – Find GCD

Problem 4 – Batting Strike Rate Calculator



















Problem 5 – Get String Length (Custom)





















Problem 6 – Copy a Word (CharArray Copy)

























 
Assignment 3 – 2D Arrays, Overloading & C-Strings
Additional set of6 programs covering 2D arrays, function overloading, and C-style string manipulation.
Program 1 – SumofAll Elements in a 2D Array

























Program 2 – Subtract All Elements from the First































Program 3 – Area Calculator (Function Overloading)


























Program 4 – Bowling Average Calculator






















Program 5 – Print a Word Vertically
























Program 6 – Reverse a Word In-Place



































Mini Project: Restaurant Billing System
Introduction
The Restaurant Billing System is a beginner-level C++ program used to manage a customer's food order and calculate the ﬁnal restaurant bill. The program takes customer details, shows a food menu, allows the user to place orders, and then calculates service charges, GST, discount, and total payable amount.
Purpose
The main purpose ofthis program is to make the billing process easy for a restaurant. It reduces manual calculation and gives the ﬁnal bill according to selected food items and quantity.
Main Features
 	Customer registration
 	Food menu display
 	Order placing
 	Service charges calculation
 	GST calculation
 	Discount calculation
 	Final bill display
 	Customer details view
Working ofProgram
First, the program asks for customer name, contact number, order type, and number of persons. After this, a menu is shown to the user. The user selects food items and enters quantity. The program adds the price ofall selected items into the food bill.
When the bill is calculated, the program applies:
 	Service charges: 10% for Dine-in and 5% for Takeaway
 	GST: 16%
 	Discount: based on the food bill amount Finally, the program displays the complete bill. Code


#include <iostream>
using namespace std;


string customerName, contactNumber, orderType;
int persons;


string foodName[8] = {" Chicken Burger", " Zinger Burger", " Pizza Small", " Pizza
" Chicken Biryani", " BBQ Platter", " Fries", " Cold Drink"};
int foodPrices[8] = {450, 550, 900, 1800, 380, 1200, 250, 120};
float foodBill = 0;


void registerCustomer() {
cout << " Enter customer name: ";
cin. ignore() ;
getline( cin,  customerName) ;


cout << " Enter contact Number: ";
cin >> contactNumber;


cout << " Enter order type ( Dine- in/Takeaway) : ";
cin >> orderType;


cout << " Enter number of persons: ";
cin >> persons;
}


void showMenu() {
cout << "\n===== Food Menu =====" << endl;
for ( int i = 0; i < 8; i++)
cout << i + 1 << ". " << foodName[i] << " Rs. " << foodPrices[i] << end
}


void placeOrder() { int item, quantity; char again;
do {
showMenu() ;
cout << " Enter item number: ";
cin >> item;
cout << " Enter quantity: ";
cin >> quantity;


if ( item >= 1 && item <= 8 && quantity > 0)
foodBill = foodBill + foodPrices[item - 1] * quantity;
else
cout << " Invalid item or quantity! " << endl;


cout << " Order more? ( y/n) : ";
cin >> again;
} while ( again == ' y' | | again == ' Y' ) ;
}


float serviceCharges() {
if ( orderType == " Dine- in" | | orderType == " dine- in")
return foodBill * 0. 10;
else
return foodBill * 0. 05;
}


float gst() {
return foodBill * 0. 16;
}


float discount() {
if ( foodBill >= 3000 && foodBill <= 5000) return foodBill * 0. 05;
else if ( foodBill > 5000 && foodBill <= 10000) return foodBill * 0. 10;
else if ( foodBill > 10000) return foodBill * 0. 15;
else return 0;
}


void showBill() {
float service = serviceCharges() ;
float tax = gst() ;
float disc = discount() ;
float total = foodBill + service + tax - disc;


cout << "\n===== RESTAURANT BILL =====" << endl;
cout << " Customer Name: " << customerName << endl;
cout << " Order Type: " << orderType << endl;
cout << " Number of Persons: " << persons << endl;
cout << " Food Bill: Rs. " << foodBill << endl;
cout << " Service Charges: Rs. " << service << endl;
cout << " GST: Rs. " << tax << endl;
cout << " Discount: Rs. " << disc << endl;


if ( total > 5000)
cout << " Free Delivery Added" << endl;


cout << " Total Payable Amount: Rs. " << total << endl;
cout << " Enjoy Your Meal : ) " << endl;
}


void showDetails() {









































Dry Run
Input










Calculation


Chicken Burger price = 450 →	2	burgers	= 450	×	2	=	900
Cold Drink price	= 120 →	2	drinks	= 120	×	2	=	240
Food Bill = 900 + 240 = 1140			
Service Charges = 1140 × 10%	=	114	
GST	= 1140 × 16%	=	182. 4	




Output





Food Bill	:	Rs.	1140
Service Charges	:	Rs.	114
GST	:	Rs.	182. 4
Discount	:	Rs.	0
Total Payable Amount :	Rs.	1436. 4

MCQs – Chapters 2, 3 & 4
Chapter 2: Introduction to C++
1.	Which data type stores whole numbers? A) ﬂoat B) int C) char D) string Answer: B
2.	What is the result ofassigning 3.88 to an int variable? A) 3.88 B) 4 C) 3 D) Error
Answer: C
3.	Which is a character constant? A) "A" B) 'A' C) A D) "A' Answer: B
4.	What does	do? A) Ends program B) Starts loop C) Moves to next line D) Deletes
output Answer: C
5.	What is a variable? A) Fixed value B) Memory location with changing value C) Operator D) Function Answer: B
Chapter 3: Expressions and Interactivity


1.	What is
Answer: B

used for? A) Looping B) Type conversion C) Input D) Output

2.	Overﬂow occurs when: A) Value is too small B) Value is too large C) Value is correct D) Value is zero Answer: B

3.	Which is a named constant? A)

B)

C)

D)

Answer: B

4.	What does the
Answer: B

operator do? A) Multiply B) Add and assign C) Divide D) Compare

5.	Which function reads a full line (with spaces)? A)	B)	C)
D)	Answer: B


Chapter 4: Making Decisions
1.	Which logical operator means AND? A)


B)


C)


D)


Answer: B

2.	Which value represents false? A) 1 B) -1 C) 0 D) 2 Answer: C
3.	What does	use? A) ﬂoat B) string C) integer/char D) array Answer: C

4.	What is the purpose of

in

? A) Continue loop B) Exit switch C) Start

program D) Compare values Answer: B

5.	What is an
Answer: C

? A) Loop B) Function C) User-deﬁned data type D) Operator


 
🛠 How to Compile & Run
Each program can be compiled individually with	:




📌 Notes
 	Some snippets above were transcrib may contain small syntax slips (e.g., been kept faithful to the original sou
 	This repository is intended for perso Fundamentals course.
