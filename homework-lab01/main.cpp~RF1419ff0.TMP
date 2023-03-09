#include <iostream>
#include <vector>
#include <algorithm>
#include <numeric>
using namespace std;

class Student{
private:
    string name;
    string surname;
    string album;
    vector<float> grades;
public:
    void set_name(string new_name){
        name = new_name;
    }
    void set_surname(string new_surname){
        surname = new_surname;
    }
    bool set_album(string new_album){
        if(new_album.size()==6 || new_album.size()==5){
            album = new_album;
            return true;
        }
        else return false;
    }
    void summary(){
        cout << "Name: " << name << endl;
        cout << "Surname: " << surname << endl;
        cout << "Album number: " << album << endl;
        cout << "Grades: ";
        for(auto grade : grades){
            cout << grade << ", ";
        }
        cout << endl;
    }
    bool add_grade(float grade){
        if(grade > 1 && grade < 6){
            grades.push_back(grade);
            return true;
        }
        else return false;
    }
    void mean(){
        cout << "Mean grade for " << name << " " << surname << "is: ";
        cout << accumulate(grades.begin(), grades.end(), 0.0f) / grades.size() << endl;
    }
    bool if_passed(){
        int counter = 0;
        for(auto grade : grades){
            if(grade == 2)
                counter++;
        }
        if(counter < 2)
            return true;
        else return false;
    }

};

int main()
{
    Student student1;
    student1.set_name("Jan");
    student1.set_surname("Kowalski");
    student1.set_album("12345");
    student1.add_grade(5);
    student1.add_grade(1);
    student1.add_grade(2);
    student1.add_grade(3);
    student1.add_grade(2);
    student1.add_grade(4);
    student1.add_grade(6);
    student1.mean();
    student1.summary();
    cout << student1.if_passed() << endl;
    return 0;
}
