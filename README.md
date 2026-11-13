#include <iostream>
#include <iomanip>
#include <string>

using namespace std;

int main() {
    string correctPassword = "WalangKanenBusseng?123";
    string password;

    cout << "STUDENT LOGIN" << endl;
    cout << "****************************************" << endl;
    cout << "Enter Password: ";
    cin >> password;

    while (password != correctPassword) {
        cout << "Incorrect Password!" << endl;
        cout << "Please try again: ";
        cin >> password;
    }

    cout << "Login Successful!" << endl;
    cout << "****************************************" << endl;
    cout << "STUDENT GRADE REPORT" << endl;
    cout << "**********************************" << endl;
    cout << "Name: CIMAFRANCA,JAYMARK" << endl;
    cout << "Year and Section: BSIT 1A" << endl;
    cout << "****************************************" << endl;
    cout << "SUBJECT GRADES" << endl;
    cout << "****************************************" << endl;

    string subjects[5] = {"Programming 1", "Database", "Networking", "Operating System", "NSTP"};
    int grades[5] = {98, 99, 98, 97, 95};

    for (int i = 0; i < 5; i++) {
        cout << subjects[i] << endl;
    }

    int total = 0;
    for (int i = 0; i < 5; i++) {
        cout << grades[i] << endl;
        total += grades[i];
    }

    double average = total / 5.0;
    string remarks = (average >= 75.0) ? "PASSED" : "FAILED";

    cout << "Total: " << total << endl;
    cout << fixed << setprecision(1);
    cout << "Average: " << average << endl;
    cout << "Overall Remarks: " << remarks << endl;

    return 0;
}
