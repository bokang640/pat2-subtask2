# pat2-subtask2

#include <iostream>


using namespace std;

int main(){
   char letters[26] =
    {
        'A','B','C','D','E','F','G','H','I','J',
        'K','L','M','N','O','P','Q','R','S','T',
        'U','V','W','X','Y','Z'
    };
    string morse[26] =
    {
        ".-","-...","-.-.","-..",".",
        "..-.","--.","....","..",".---",
        "-.-",".-..","--","-.","---",
        ".--.","--.-",".-.","...","-",
        "..-","...-",".--","-..-","-.--","--.."
    };

 string message;
    string fullMessage = "";

   // Ask user for input
    cout << "Enter a message in English (A-Z characters only): ";
    getline(cin, message);

  // Convert message to uppercase
    for (int i = 0; i < message.length(); i++)
    {
        message[i] = toupper(message[i]);
    }

   cout << endl;
 

 // Loop through each character
    for (int i = 0; i < message.length(); i++)
    {
        char currentLetter = message[i];
 // Ignore spaces
        if (currentLetter == ' ')
        {
            fullMessage += "   ";
        }

 // Check letters A-Z
         for (int j = 0; j < 26; j++)
        {
   if (currentLetter == letters[j])
    {
    // Display individual letter and Morse code
   cout << currentLetter << ": " << morse[j] << endl;

 // Add to full Morse message
fullMessage += morse[j] + "   ";
        }
        }
    } // Display full Morse code message
    cout << endl;
    cout << "Full Morse Code Message:";
    cout << fullMessage << endl;
 return 0;
}


return 0;}
