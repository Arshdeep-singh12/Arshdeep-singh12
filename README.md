#include <iostream>
#include <vector> 
using namespace std;

class employee {
    vector<int> e;
    string name;

    static int employee_count; 
    int id;
    int hours_worked;
    int salary; 
public:
    void add() {
        cout << "enter the id of the employee : " << endl;
        cin >> id;
        cout << "enter the hours worked by the employee : " << endl;
        cin >> hours_worked;
        e.push_back(id);
        e.push_back(hours_worked);
        employee_count++;
    }
    void cal_sar() {
        int total = hours_worked * 600;
        salary = total;
        e.push_back(salary);
    }
    void disp() {
        cout<<"id\thours worked\tsalary"<<endl;
    for (int i = 0; i < e.size(); i += 3) { 
        for(int j = 0; j < 3; j++) {
            cout << e[i + j] << "\t"; 
        }
        cout << endl;
    }
}

    
};

int employee::employee_count = 0;

int main() {
    int n;
    employee e1;
    while (1) { 
        cout << "enter 1 add 2 to display information of the employee, 0 to exit: " << endl;
        cin >> n;
        switch (n) {
        case 1:
            e1.add();
            e1.cal_sar();
            break; 
        case 2:
            e1.disp();
            break; 
        
        
        }
    }
}
