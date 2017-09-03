# HTML++
Code to handle HTML forms and AJAX post requests for C++.
It doesn't support GET but this should be easy to update.

Format:

#include <iostream> // has string as well
#include "postcgi" // only with "" in the same directory

int main(){
    cout << "Document-Type: application/json" << endl << endl;
    Post post;
    if (post.get("date") != "false"){
        string date = post.get("date");
    }
    return 0;
}

or 

    string date = post.get("date");
    if (date != "false"){
        // use date for something
    }
