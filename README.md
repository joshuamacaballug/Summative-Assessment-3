# Summative-Assessment-3
#include <iostream>
#include <math.h>
#include <string>
#include <stdlib.h>
#include <windows.h>
#ifndef NOMINMAX
#define NOMINMAX
#endif
using namespace std;
void setcolor(unsigned char color)
{
	SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE), color);
}
int main()
{
	system("Color 0A");
	cout << "|============================================================|\n|";
	setcolor(0x0F);
	cout << " Welcome to SbarTucks Coffee! Please enter costumer's name: ";
	setcolor(0x0A);
	cout << "|\n|============================================================|\n";
	{
		{
			string costumerName;
			getline(cin, costumerName);
			setcolor(0x0F);
			cout << "Good day costumer, ";
			setcolor(0x0E);
			cout << costumerName << "!\n";
			setcolor(0x0A);
			cout << "|=======================================|\n";
			setcolor(0x0A);
			cout << "|";
			setcolor(0x0F);
			cout << " Would you like a ";
			setcolor(0x0B);
			cout << "Tea";
			setcolor(0x0F);
			cout << " or ";
			setcolor(0x0B);
			cout << "Coffee";
			setcolor(0x0F);
			cout << "? [T/C]:";
			setcolor(0x0A);
			cout << "|\n";
			setcolor(0x0A);
			cout << "|=======================================|\n";
			char input;
			cin >> input;
			switch (input) {
			case 'T': {
				setcolor(0x0A);
				cout << "|============================================================|\n|";
				setcolor(0x0F);
				cout << "Please type a valid number of your chosen drink: [1] [2] [3]";
				setcolor(0x0A);
				cout << "|\n|============================================================|\n";
				setcolor(0x0F);
				cout << "|              |           PRICE             |               |\n";
				cout << "|              |-----------------------------|               |\n";
				cout << "|              | [1] Iced Tea         3 AED  |               |\n";
				cout << "|              | [2] Milk Tea         2 AED  |               |\n";
				cout << "|              | [3] Black Tea        1 AED  |               |\n";
				setcolor(0x0A);
				cout << "|============================================================|\n";
				setcolor(0x0F);
				int tt;
				cin >> tt;
				if (tt == 1) {
					cout << "Iced Tea it is!\n";
					cout << "Would you like to add more sugar? (Additional 1 AED)\n YES or NO? [Y/N]:";
					char pp;
					cin >> pp;
					while ((pp != 'Y') && (pp != 'N'))
					{
						setcolor(0x0C);
						cout << "[ERROR]: Invalid response, try again:\n" << endl;
						cin >> pp;
						setcolor(0x0F);
					}
					if (pp == 'Y') {
						cout << "Alright!\nPouring Sugar..\nYour total amount is: 4 AED.\n";
						cout << "Please enter the amount of your payment:";
						setcolor(0x0F);
						int pc;
						cin >> pc;
						while ((pc < 4) || (cin.fail())) {
							cin.clear();
							cin.ignore(1000, '\n');
							setcolor(0x0C);
							cout << "[ERROR]: Invalid response, try again:\n" << endl;
							setcolor(0x0F);
							cin >> pc;
						}
						setcolor(0x0A);
						cout << "Payment recieved!\n";
						setcolor(0x0F);
						cout << "Your change is: ";
						cout << pc - 4 << "AED\nThank you for choosing SbarTucks costumer, ";
						setcolor(0x0E);
						cout << costumerName << "!";
						setcolor(0x0F);
						break;
					}
					else if (pp == 'N'){
						setcolor(0x0F);
						cout << "Alright, no sugar added.\nYour total amount is: 3 AED.\n";
						cout << "Please enter the amount of your payment:";
						int pt;
						cin >> pt;
						while ((pt < 3) || (cin.fail())) {
							cin.clear();
							cin.ignore(1000, '\n');
							setcolor(0x0C);
							cout << "[ERROR]: Invalid response, try again:\n" << endl;
							setcolor(0x0F);
							cin >> pt;
						}
						setcolor(0x0A);
						cout << "Payment recieved!\n";
						setcolor(0x0F);
						cout << "Your change is: ";
						cout << pt - 3 << "AED\nThank you for choosing SbarTucks costumer, ";
						setcolor(0x0E);
						cout << costumerName << "!";
						setcolor(0x0F);
						break;
					}
				}
				else if (tt == 2) {
					cout << "Milk Tea it is!\nWould you like to add more sugar? (Additional 1 AED)\n YES or NO? [Y/N]:";
					char yy;
					cin >> yy;
					while ((yy != 'Y') && (yy != 'N'))
					{
						setcolor(0x0C);
						cout << "[ERROR]: Invalid response, try again:\n" << endl;
						cin >> yy;
						setcolor(0x0F);
					}
					if (yy == 'Y') {
						cout << "Alright!\nPouring Sugar..\nYour total amount is: 3 AED.\n";
						cout << "Please enter the amount of your payment:";
						int ee;
						cin >> ee;
						while ((ee < 3) || (cin.fail())) {
							cin.clear();
							cin.ignore(1000, '\n');
							setcolor(0x0C);
							cout << "[ERROR]: Invalid response, try again:\n" << endl;
							setcolor(0x0F);
							cin >> ee;
						}
						setcolor(0x0A);
						cout << "Payment recieved!\n";
						setcolor(0x0F);
						cout << "Your change is: ";
						cout << ee - 3 << "AED\nThank you for choosing SbarTucks costumer, ";
						setcolor(0x0E);
						cout << costumerName << "!";
						setcolor(0x0F);
						break;
					}
					else if (yy == 'N') {
						cout << "Alright, no sugar added.\nYour total amount is: 2 AED.\n";
						cout << "Please enter the amount of your payment:";
						int qq;
						cin >> qq;
						while ((qq < 2) || (cin.fail())) {
							cin.clear();
							cin.ignore(1000, '\n');
							setcolor(0x0C);
							cout << "[ERROR]: Invalid response, try again:\n" << endl;
							setcolor(0x0F);
							cin >> qq;
						}
						setcolor(0x0A);
						cout << "Payment recieved!\n";
						setcolor(0x0F);
						cout << "Your change is: ";
						cout << qq - 2 << "AED\nThank you for choosing SbarTucks costumer, ";
						setcolor(0x0E);
						cout << costumerName << "!";
						setcolor(0x0F);
						break;
					}
				}
				else if (tt == 3) {
					cout << "Black Tea it is!\nWould you like to add more sugar? (Additional 1 AED)\n YES or NO? [Y/N]:";
					char vv;
					cin >> vv;
					while ((vv != 'Y') && (vv != 'N'))
					{
						setcolor(0x0C);
						cout << "[ERROR]: Invalid response, try again:\n" << endl;
						cin >> vv;
						setcolor(0x0F);
					}
					if (vv == 'Y') {
						cout << "Alright!\nPouring Sugar..\nYour total amount is: 2 AED.\n";
						cout << "Please enter the amount of your payment:";
						int aa;
						cin >> aa;
						while ((aa < 2) || (cin.fail())) {
							cin.clear();
							cin.ignore(1000, '\n');
							setcolor(0x0C);
							cout << "[ERROR]: Invalid response, try again:\n" << endl;
							setcolor(0x0F);
							cin >> aa;
						}
						setcolor(0x0A);
						cout << "Payment recieved!\n";
						setcolor(0x0F);
						cout << "Your change is: ";
						cout << aa - 2 << "AED\nThank you for choosing SbarTucks costumer, ";
						setcolor(0x0E);
						cout << costumerName << "!";
						setcolor(0x0F);
						break;
					}
					else if (vv == 'N') {
						cout << "Alright, no sugar added.\nYour total amount is: 1 AED.\n";
						cout << "Please enter the amount of your payment:";
						int zz;
						cin >> zz;
						while ((zz < 1) || (cin.fail())) {
							cin.clear();
							cin.ignore(1000, '\n');
							setcolor(0x0C);
							cout << "[ERROR]: Invalid response, try again:\n" << endl;
							setcolor(0x0F);
							cin >> zz;
						}
						setcolor(0x0A);
						cout << "Payment recieved!\n";
						setcolor(0x0F);
						cout << "Your change is: ";
						cout << zz - 1 << "AED\nThank you for choosing SbarTucks costumer, ";
						setcolor(0x0E);
						cout << costumerName << "!";
						setcolor(0x0F);
						break;
					}
				}
			}
			case 'C': {

				setcolor(0x0A);
				cout << "|============================================================|\n|";
				setcolor(0x0F);
				cout << "Please type a valid number of your chosen drink: [1] [2] [3]";
				setcolor(0x0A);
				cout << "|\n|============================================================|\n";
				setcolor(0x0F);
				cout << "|              |           PRICE             |               |\n";
				cout << "|              |-----------------------------|               |\n";
				cout << "|              | [1] Iced Coffee      3 AED  |               |\n";
				cout << "|              | [2] Milk Coffee      2 AED  |               |\n";
				cout << "|              | [3] Black Coffee     1 AED  |               |\n";
				setcolor(0x0A);
				cout << "|============================================================|\n";
				setcolor(0x0F);
				int oo;
				cin >> oo;
				if (oo == 1) {
					cout << "Iced Coffee it is!\nWould you like to add more sugar? (Additional 1 AED)\n YES or NO? [Y/N]:";
					char ii;
					cin >> ii;
					while ((ii != 'Y') && (ii != 'N'))
					{
						setcolor(0x0C);
						cout << "[ERROR]: Invalid response, try again:\n" << endl;
						cin >> ii;
						setcolor(0x0F);
					}
					if (ii == 'Y') {
						cout << "Alright!\nPouring Sugar..\nYour total amount is: 4 AED.\n";
						cout << "Please enter the amount of your payment:";
						int rt;
						cin >> rt;
						while ((rt < 4) || (cin.fail())) {
							cin.clear();
							cin.ignore(1000, '\n');
							setcolor(0x0C);
							cout << "[ERROR]: Invalid response, try again:\n" << endl;
							setcolor(0x0F);
							cin >> rt;
						}
						setcolor(0x0A);
						cout << "Payment recieved!\n";
						setcolor(0x0F);
						cout << "Your change is: ";
						cout << rt - 4 << "AED\nThank you for choosing SbarTucks costumer, ";
						setcolor(0x0E);
						cout << costumerName << "!";
						setcolor(0x0F);
						break;
					}
					else if (ii == 'N') {
						cout << "Alright, no sugar added.\nYour total amount is: 3 AED.\n";
						cout << "Please enter the amount of your payment:";
						int er;
						cin >> er;
						while ((er < 3) || (cin.fail())) {
							cin.clear();
							cin.ignore(1000, '\n');
							setcolor(0x0C);
							cout << "[ERROR]: Invalid response, try again:\n" << endl;
							setcolor(0x0F);
							cin >> er;
						}
						setcolor(0x0A);
						cout << "Payment recieved!\n";
						setcolor(0x0F);
						cout << "Your change is: ";
						cout << er - 3 << "AED\nThank you for choosing SbarTucks costumer, ";
						setcolor(0x0E);
						cout << costumerName << "!";
						setcolor(0x0F);
						break;
					}
				}
				else if (oo == 2) {
					cout << "Milk Coffee it is!\nWould you like to add more sugar? (Additional 1 AED)\n YES or NO? [Y/N]:";
					char wq;
					cin >> wq;
					while ((wq != 'Y') && (wq != 'N'))
					{
						setcolor(0x0C);
						cout << "[ERROR]: Invalid response, try again:\n" << endl;
						cin >> wq;
						setcolor(0x0F);
					}
					if (wq == 'Y') {
						cout << "Alright!\nPouring Sugar..\nYour total amount is: 3 AED.\n";
						cout << "Please enter the amount of your payment:";
						int ds;
						cin >> ds;
						while ((ds < 3) || (cin.fail())) {
							cin.clear();
							cin.ignore(1000, '\n');
							setcolor(0x0C);
							cout << "[ERROR]: Invalid response, try again:\n" << endl;
							setcolor(0x0F);
							cin >> ds;
						}
						setcolor(0x0A);
						cout << "Payment recieved!\n";
						setcolor(0x0F);
						cout << "Your change is: ";
						cout << ds - 3 << "AED\nThank you for choosing SbarTucks costumer, ";
						setcolor(0x0E);
						cout << costumerName << "!";
						setcolor(0x0F);
						break;
					}
					else if (wq == 'N') {
						cout << "Alright, no sugar added.\nYour total amount is: 2 AED.\n";
						cout << "Please enter the amount of your payment:";
						int xc;
						cin >> xc;
						while ((xc < 2) || (cin.fail())) {
							cin.clear();
							cin.ignore(1000, '\n');
							setcolor(0x0C);
							cout << "[ERROR]: Invalid response, try again:\n" << endl;
							setcolor(0x0F);
							cin >> xc;
						}
						setcolor(0x0A);
						cout << "Payment recieved!\n";
						setcolor(0x0F);
						cout << "Your change is: ";
						cout << xc - 2 << "AED\nThank you for choosing SbarTucks costumer, ";
						setcolor(0x0E);
						cout << costumerName << "!";
						setcolor(0x0F);
						break;
					}
				}
				else if (oo == 3) {
					cout << "Black Coffee it is!\nWould you like to add more sugar? (Additional 1 AED)\n YES or NO? [Y/N]:";
					char bv;
					cin >> bv;
					while ((bv != 'Y') && (bv != 'N'))
					{
						setcolor(0x0C);
						cout << "[ERROR]: Invalid response, try again:\n" << endl;
						cin >> bv;
						setcolor(0x0F);
					}
					if (bv == 'Y') {
						cout << "Alright!\nPouring Sugar..\nYour total amount is: 2 AED.\n";
						cout << "Please enter the amount of your payment:";
						int fg;
						cin >> fg;
						while ((fg < 2) || (cin.fail())) {
							cin.clear();
							cin.ignore(1000, '\n');
							setcolor(0x0C);
							cout << "[ERROR]: Invalid response, try again:\n" << endl;
							setcolor(0x0F);
							cin >> fg;
						}
						setcolor(0x0A);
						cout << "Payment recieved!\n";
						setcolor(0x0F);
						cout << "Your change is: ";
						cout << fg - 2 << "AED\nThank you for choosing SbarTucks costumer, ";
						setcolor(0x0E);
						cout << costumerName << "!";
						setcolor(0x0F);
						break;
					}
					else if (bv == 'N') {
						cout << "Alright, no sugar added.\nYour total amount is: 1 AED.\n";
						cout << "Please enter the amount of your payment:";
						int df;
						cin >> df;
						while ((df < 1) || (cin.fail())) {
							cin.clear();
							cin.ignore(1000, '\n');
							setcolor(0x0C);
							cout << "[ERROR]: Invalid response, try again:\n" << endl;
							setcolor(0x0F);
							cin >> df;
						}
						setcolor(0x0A);
						cout << "Payment recieved!\n";
						setcolor(0x0F);
						cout << "Your change is: ";
						cout << df - 1 << "AED\nThank you for choosing SbarTucks costumer, ";
						setcolor(0x0E);
						cout << costumerName << "!";
						setcolor(0x0F);
						break;
					}
				}
			}
			}
			}
		}
	}
