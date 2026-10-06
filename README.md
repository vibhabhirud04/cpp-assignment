#include <iostream>
#include <string>
using namespace std;

// Node structure
struct Passenger {
    int id;
    string name;
    int age;
    Passenger* next;
};

Passenger* head = NULL;

// Function to add passenger
void addPassenger() {
    Passenger* p = new Passenger;

    cout << "\nEnter Passenger ID: ";
    cin >> p->id;

    cout << "Enter Passenger Name: ";
    cin >> p->name;

    cout << "Enter Passenger Age: ";
    cin >> p->age;

    p->next = NULL;

    if (head == NULL) {
        head = p;
    }
    else {
        Passenger* temp = head;

        while (temp->next != NULL) {
            temp = temp->next;
        }

        temp->next = p;
    }

    cout << "Passenger added successfully.\n";
}

// Function to delete passenger
void deletePassenger() {
    int id;

    cout << "\nEnter Passenger ID to delete: ";
    cin >> id;

    if (head == NULL) {
        cout << "No passenger records found.\n";
        return;
    }

    // If first passenger is to be deleted
    if (head->id == id) {
        Passenger* temp = head;
        head = head->next;
        delete temp;

        cout << "Passenger deleted successfully.\n";
        return;
    }

    Passenger* temp = head;

    while (temp->next != NULL && temp->next->id != id) {
        temp = temp->next;
    }

    if (temp->next == NULL) {
        cout << "Passenger not found.\n";
    }
    else {
        Passenger* del = temp->next;
        temp->next = del->next;
        delete del;

        cout << "Passenger deleted successfully.\n";
    }
}

// Function to search passenger
void searchPassenger() {
    int id;

    cout << "\nEnter Passenger ID to search: ";
    cin >> id;

    Passenger* temp = head;

    while (temp != NULL) {
        if (temp->id == id) {
            cout << "\nPassenger Found!\n";
            cout << "Passenger ID   : " << temp->id << endl;
            cout << "Passenger Name : " << temp->name << endl;
            cout << "Passenger Age  : " << temp->age << endl;

            return;
        }

        temp = temp->next;
    }

    cout << "Passenger not found.\n";
}

// Function to display all passengers
void displayPassengers() {
    if (head == NULL) {
        cout << "\nNo passenger records found.\n";
        return;
    }

    Passenger* temp = head;

    cout << "\n----- Train Passenger Records -----\n";

    while (temp != NULL) {
        cout << "Passenger ID   : " << temp->id << endl;
        cout << "Passenger Name : " << temp->name << endl;
        cout << "Passenger Age  : " << temp->age << endl;
        cout << "----------------------------------\n";

        temp = temp->next;
    }
}

// Main function
int main() {
    int choice;

    do {
        cout << "\n===== TRAIN PASSENGER RECORD SYSTEM =====";
        cout << "\n1. Add Passenger";
        cout << "\n2. Delete Passenger";
        cout << "\n3. Search Passenger";
        cout << "\n4. Display Passengers";
        cout << "\n5. Exit";

        cout << "\nEnter your choice: ";
        cin >> choice;

        switch (choice) {
            case 1:
                addPassenger();
                break;

            case 2:
                deletePassenger();
                break;

            case 3:
                searchPassenger();
                break;

            case 4:
                displayPassengers();
                break;

            case 5:
                cout << "\nExiting program...\n";
                break;

            default:
                cout << "\nInvalid choice! Please try again.\n";
        }

    } while (choice != 5);

    return 0;
}#include <iostream>
#include <string>
using namespace std;

// Node structure
struct Passenger {
    int id;
    string name;
    int age;
    Passenger* next;
};

Passenger* head = NULL;

// Function to add passenger
void addPassenger() {
    Passenger* p = new Passenger;

    cout << "\nEnter Passenger ID: ";
    cin >> p->id;

    cout << "Enter Passenger Name: ";
    cin >> p->name;

    cout << "Enter Passenger Age: ";
    cin >> p->age;

    p->next = NULL;

    if (head == NULL) {
        head = p;
    }
    else {
        Passenger* temp = head;

        while (temp->next != NULL) {
            temp = temp->next;
        }

        temp->next = p;
    }

    cout << "Passenger added successfully.\n";
}

// Function to delete passenger
void deletePassenger() {
    int id;

    cout << "\nEnter Passenger ID to delete: ";
    cin >> id;

    if (head == NULL) {
        cout << "No passenger records found.\n";
        return;
    }

    // If first passenger is to be deleted
    if (head->id == id) {
        Passenger* temp = head;
        head = head->next;
        delete temp;

        cout << "Passenger deleted successfully.\n";
        return;
    }

    Passenger* temp = head;

    while (temp->next != NULL && temp->next->id != id) {
        temp = temp->next;
    }

    if (temp->next == NULL) {
        cout << "Passenger not found.\n";
    }
    else {
        Passenger* del = temp->next;
        temp->next = del->next;
        delete del;

        cout << "Passenger deleted successfully.\n";
    }
}

// Function to search passenger
void searchPassenger() {
    int id;

    cout << "\nEnter Passenger ID to search: ";
    cin >> id;

    Passenger* temp = head;

    while (temp != NULL) {
        if (temp->id == id) {
            cout << "\nPassenger Found!\n";
            cout << "Passenger ID   : " << temp->id << endl;
            cout << "Passenger Name : " << temp->name << endl;
            cout << "Passenger Age  : " << temp->age << endl;

            return;
        }

        temp = temp->next;
    }

    cout << "Passenger not found.\n";
}

// Function to display all passengers
void displayPassengers() {
    if (head == NULL) {
        cout << "\nNo passenger records found.\n";
        return;
    }

    Passenger* temp = head;

    cout << "\n----- Train Passenger Records -----\n";

    while (temp != NULL) {
        cout << "Passenger ID   : " << temp->id << endl;
        cout << "Passenger Name : " << temp->name << endl;
        cout << "Passenger Age  : " << temp->age << endl;
        cout << "----------------------------------\n";

        temp = temp->next;
    }
}

// Main function
int main() {
    int choice;

    do {
        cout << "\n===== TRAIN PASSENGER RECORD SYSTEM =====";
        cout << "\n1. Add Passenger";
        cout << "\n2. Delete Passenger";
        cout << "\n3. Search Passenger";
        cout << "\n4. Display Passengers";
        cout << "\n5. Exit";

        cout << "\nEnter your choice: ";
        cin >> choice;

        switch (choice) {
            case 1:
                addPassenger();
                break;

            case 2:
                deletePassenger();
                break;

            case 3:
                searchPassenger();
                break;

            case 4:
                displayPassengers();
                break;

            case 5:
                cout << "\nExiting program...\n";
                break;

            default:
                cout << "\nInvalid choice! Please try again.\n";
        }

    } while (choice != 5);

    return 0;
}
