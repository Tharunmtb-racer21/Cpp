#include <iostream>
#include <fstream>
using namespace std;

int main() {
    ofstream writeFile("data.txt");
    writeFile << "This is the first line in the file.\n";
    writeFile.close();

    ofstream appendFile("data.txt", ios::app);
    appendFile << "This line is appended to the file.\n";
    appendFile.close();

    ifstream readFile("data.txt");
    string line;
    cout << "File Contents:\n";
    while (getline(readFile, line)) {
        cout << line << endl;
    }
    readFile.close();

    return 0;
}
