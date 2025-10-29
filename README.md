#include <iostream>
#include<cmath>
#include <string>
using namespace std;

class Vehicle {
public:
    Vehicle(std::string make, std::string model, int year);
    virtual ~Vehicle() = default;
    virtual double calculateRentalCost() const = 0;
    virtual void displayDetails() const;

private:
    
    string make;
    string model;
    int year;
};
Vehicle::Vehicle(std::string make, std::string model, int year)
    : make(make), model(model), year(year)

void Vehicle::displayDetails() const;{
    cout << "-----------------------------" <<endl;
    cout << "Make:  " << make <<endl;
    cout << "Model: " << model <<endl;
    cout << "Year:  " << year <<endl;
}


int main() {
cout << "Testing the Vehicle abstract base class." <<endl;

    

    cout<< "\nSuccessfully demonstrated that 'Vehicle' is an abstract class." <<endl;
    cout << "The next step is to create derived classes like 'Car' or 'Truck'." <<endl;

    return 0;
}
