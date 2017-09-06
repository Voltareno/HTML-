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

I am preparing functions size, begin and end to measure/locate number of character inside the post string.
What is still not working and needs to be done is similar keys.
For example if we are looking for "key" and there is post name "keys".
In this case the program will throw an error.
    begin = -1
    end = -1
This is ok for now but later I would like to improve in case there is input name keys and then second input named key.
That will be done in the future.
Another feature coming up is substr in case of wide/multibyte chars. Which doesn't work with simple string substr.
