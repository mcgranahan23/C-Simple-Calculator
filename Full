
#include <iostream>

using namespace std;

int main() // Changed to int main, void main causes errors
{
    // Deleted char statement[100] because it wasn't used
    int op1, op2;
    char operation;
    bool answer = true; // Changed to boolean since there are only two options, less room for error
    char tempAns; // Temp variable used at the end
    bool tempSwitch = false; // Temp variable used at the end
    bool isDigit = false;
    
    while (answer) // Changed to continue loop while answer = true
    {
        tempSwitch = false; // This is placed here to reset the variable, if it's not here it remains true
        isDigit = false;
        
        do { // Do while loop so the expression is evaluated after contents of loop
            cout << "Enter expression" << endl;
            cin >> op1 >> operation >> op2; // Switched op1 & op2 because that's the order they are entered
            
            if (!cin.fail()) { // cin.fail is used so if input is anything but an int, the error message will print and run again
                isDigit = true;
            }
            else { 
                cout << "Please enter a digit, operation, and another digit." << endl;
                cin.clear();
                cin.ignore(100, '\n'); // cin.clear clears the stream to avoid endless loop, cin.ignore ignores the next 100 characters and the new line
            }
            
            
        } while (!isDigit); // !isDigit is the temp variable made for this loop, will run until it's changed to true
        
        // Replaced multiple if statements with a switch to make code more clear and also run better
        switch (operation) {
            case '+':
                cout << op1 << " + " << op2 << " = " << op1 + op2 << endl;
                break;
            case '-':
                cout << op1 << " - " << op2 << " = " << op1 - op2 << endl;
                break;
            case '*':
                cout << op1 << " * " << op2 << " = " << op1 * op2 << endl;
                break;
            case '/':
                cout << op1 << " / " << op2 << " = " << op1 / op2 << endl;
                break;
            default:
                cout << "Invalid expression" << endl;
                break;
            // If the operation is invalid it falls directly below to prompt another expression
        }
        
        cout << "Do you wish to evaluate another expression? y/n" << endl; // Added y/n for clarity
        cin >> tempAns;
        tempAns = tolower(tempAns); 
        // This makes the user's answer lowercase to avoid excessive code accounting for both Y and y
        
        // The following loop takes the user's answer and runs through a switch and also verifying correct input,
        //if anything other than y or n is entered it prompts the error message and takes input again until it's correct
        
        while (!tempSwitch) {
            switch (tempAns) {
                case 'y':
                    answer = true;
                    tempSwitch = true;
                    break;
                case 'n':
                    answer = false;
                    tempSwitch = true;
                    break;
                default:
                    cout << "Invalid answer, please try again." << endl << "Do you wish to evaluate another expression? y/n";
                    cin >> tempAns;
                    break;
            }
        }
    }
    cout << "Program Finished" << endl;
    
    return 0; // Return statement to complete program
}






