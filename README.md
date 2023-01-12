"# gamedev_test" 
Azamatov Abylaikhan
<h1>Task 1</h1>
#include <iostream>
#include <string>
#include <cctype>
#include <algorithm>
#include <vector>
#include <stdio.h>
#include <cstring>
#define _CRT_SECURE_NO_WARNINGS // для возможности использования scanf
#include <stdio.h>
#include <stdlib.h> 
using namespace std;
 
int main()
{   
	const int n = 300;
 
    char text[n];
    text[n] = std::toupper(text[n]);
    std::cin.getline(text, n);
 
    int count = strlen(text);
 
    int sum = 0;
    string s = "";
 
 
    for (int i = 0; i< count; i++) {
    	for (int a = 0; a< count; a++) {
    		if (std::toupper(text[i]) == std::toupper(text[a])) {
    			sum += 1;
    		} else{
    			sum += 0;
    		}
    	}
 
 
    	if (sum != 0) {
	    	if (sum == 1) {
	    		s += "(";
	    	} else {
	    		s += ")";
	    	}
    	}
    	sum = 0;
    }
 
    std::cout<<s<<std::endl;
}
