#include <iostream>
using namespace std;
class BankAccount {
private:
    int accountNumber;
    double balance;
public:
    BankAccount(int accNum = 0, double bal = 0.0) {
        accountNumber = accNum;
        balance = bal;
    }
    void display() {
        cout << "Account Number: " << accountNumber << endl;
        cout << "Balance: $" << balance << endl;
    }
    void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
        }
    }
    void withdraw(double amount) {
        if (amount > 0 && amount <= balance) {
            balance -= amount;
        } else {
            cout << "Insufficient funds or invalid amount." << endl;
        }
    }
};
int main() {
    BankAccount acc1; 
    BankAccount acc2(12345, 500.0); 
    cout << "Account 1 details:" << endl;
    acc1.display();
    cout << "\nAccount 2 details:" << endl;
    acc2.display();
    acc2.deposit(200);
    acc2.withdraw(100);
    cout << "\nAccount 2 after transactions:" << endl;
    acc2.display();
    return 0;
}
