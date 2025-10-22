# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
'''
#include <stdio.h>

int main() {
    float length, width, area;
    float *ptrLength = &length;
    float *ptrWidth = &width;

    // Input length and width
    printf("Enter length of the rectangle: ");
    scanf("%f", ptrLength);

    printf("Enter width of the rectangle: ");
    scanf("%f", ptrWidth);

    // Calculate area using pointers
    area = (*ptrLength) * (*ptrWidth);

    // Display result
    printf("Area of the rectangle = %.2f\n", area);

    return 0;
}
'''

## OUTPUT
		       	
![Image](https://github.com/user-attachments/assets/d56a8b3e-bb31-4490-8798-d52be911a466)

## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
'''
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main() {
    // Allocate memory for 8 characters (7 letters + null terminator)
    char *str = (char *)malloc(8 * sizeof(char));

    // Check if memory allocation was successful
    if (str == NULL) {
        printf("Memory allocation failed.\n");
        return 1;
    }

    // Copy the string into allocated memory
    strcpy(str, "WELCOME");

    // Print the string
    printf("The string is: %s\n", str);

    // Free the allocated memory
    free(str);

    return 0;
}
'''

## OUTPUT

![Image](https://github.com/user-attachments/assets/2e3fdfee-969d-4a49-bdf6-152c4eed4ead)

## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
'''
#include <stdio.h>

// Define structure for student
struct Student {
    int rollNo;
    char name[50];
    float marks;
};

int main() {
    struct Student s;

    // Input student details
    printf("Enter student roll number: ");
    scanf("%d", &s.rollNo);

    printf("Enter student name: ");
    scanf(" %[^\n]", s.name);  // Reads string with spaces

    printf("Enter student marks: ");
    scanf("%f", &s.marks);

    // Display student details
    printf("\n--- Student Information ---\n");
    printf("Roll Number: %d\n", s.rollNo);
    printf("Name       : %s\n", s.name);
    printf("Marks      : %.2f\n", s.marks);

    return 0;
}
'''

## OUTPUT

![Image](https://github.com/user-attachments/assets/61e5fb9a-e08c-4590-bab4-80f680d82af9)

## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
'''
#include <stdio.h>

// Define structure for Employee
struct Employee {
    int id;
    char name[50];
    float basicSalary;
    float hra;  // House Rent Allowance
    float da;   // Dearness Allowance
    float grossSalary;
};

int main() {
    struct Employee emp[3];

    // Input employee data
    for (int i = 0; i < 3; i++) {
        printf("\nEnter details for Employee %d:\n", i + 1);

        printf("ID: ");
        scanf("%d", &emp[i].id);

        printf("Name: ");
        scanf(" %[^\n]", emp[i].name);  // Reads string with spaces

        printf("Basic Salary: ");
        scanf("%f", &emp[i].basicSalary);

        printf("HRA: ");
        scanf("%f", &emp[i].hra);

        printf("DA: ");
        scanf("%f", &emp[i].da);

        // Calculate Gross Salary
        emp[i].grossSalary = emp[i].basicSalary + emp[i].hra + emp[i].da;
    }

    // Display employee data
    printf("\n--- Employee Salary Details ---\n");
    for (int i = 0; i < 3; i++) {
        printf("\nEmployee %d:\n", i + 1);
        printf("ID           : %d\n", emp[i].id);
        printf("Name         : %s\n", emp[i].name);
        printf("Basic Salary : %.2f\n", emp[i].basicSalary);
        printf("HRA          : %.2f\n", emp[i].hra);
        printf("DA           : %.2f\n", emp[i].da);
        printf("Gross Salary : %.2f\n", emp[i].grossSalary);
    }

    return 0;
}
'''

 ## OUTPUT

 ![Image](https://github.com/user-attachments/assets/3b272389-8439-4b6c-9581-53b1029924a3)

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
'''
#include <stdio.h>

// Define structure for Student
struct Student {
    char name[50];
    int rollNo;
    float marks[5];  // Array to store marks of 5 subjects
    float total;
    float average;
};

int main() {
    struct Student s;
    int i;

    // Input student details
    printf("Enter student name: ");
    scanf(" %[^\n]", s.name);

    printf("Enter roll number: ");
    scanf("%d", &s.rollNo);

    printf("Enter marks for 5 subjects:\n");
    s.total = 0;
    for (i = 0; i < 5; i++) {
        printf("Subject %d: ", i + 1);
        scanf("%f", &s.marks[i]);
        s.total += s.marks[i];
    }

    // Calculate average
    s.average = s.total / 5;

    // Display results
    printf("\n--- Student Result ---\n");
    printf("Name     : %s\n", s.name);
    printf("Roll No  : %d\n", s.rollNo);
    printf("Total    : %.2f\n", s.total);
    printf("Average  : %.2f\n", s.average);

    return 0;
}
'''

## OUTPUT

 ![Image](https://github.com/user-attachments/assets/7178ef63-5ecf-4aed-af48-0807192fe151)

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


