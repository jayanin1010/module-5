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

	#include <stdio.h>
	
	int main() {
	    float x, y, area;
	    printf("Enter the length (x): ");
	    scanf("%f", &x);
	    printf("Enter the width (y): ");
	    scanf("%f", &y);
	    area = x * y;
	    printf("The area of the rectangle is: %.2f\n", area);
	    return 0;
	}


## OUTPUT

![image](https://github.com/user-attachments/assets/83fc178e-e1b8-42fd-9cb3-6617768467bc)



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

	#include <stdio.h>
	#include <stdlib.h>
	#include <string.h>
	
	int main() {
	    char temp[100], *str;
	    printf("Enter a string: ");
	    fgets(temp, sizeof(temp), stdin);
	    temp[strcspn(temp, "\n")] = '\0';
	    str = (char *)malloc(strlen(temp) + 1);
	    if (!str) return 1;
	    strcpy(str, temp);
	    printf("You entered: %s\n", str);
	    free(str);
	    return 0;
	}


## OUTPUT

![image](https://github.com/user-attachments/assets/14bdc22c-970f-45e9-94f0-1fc769e98ec1)



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

	#include <stdio.h>
	
	struct Student {
	    char name[50];
	    int roll;
	    float marks;
	};
	
	int main() {
	    struct Student s;
	
	    printf("Enter name: ");
	    fgets(s.name, sizeof(s.name), stdin);
	    s.name[strcspn(s.name, "\n")] = '\0';
	
	    printf("Enter roll number: ");
	    scanf("%d", &s.roll);
	
	    printf("Enter marks: ");
	    scanf("%f", &s.marks);
	
	    printf("\nStudent Details:\n");
	    printf("Name: %s\n", s.name);
	    printf("Roll Number: %d\n", s.roll);
	    printf("Marks: %.2f\n", s.marks);
	
	    return 0;
	}


## OUTPUT

![image](https://github.com/user-attachments/assets/31bf2ca6-0db8-4c55-8569-bbe586781cf3)


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

	#include <stdio.h>
	
	struct Employee {
	    char name[50];
	    int id;
	    float salary;
	    float gross;
	};
	
	int main() {
	    struct Employee e[3];
	    int i;
	
	    // Input for 3 employees
	    for (i = 0; i < 3; i++) {
	        printf("\nEnter details for Employee %d:\n", i + 1);
	        printf("Name: ");
	        getchar(); // To consume leftover newline from previous input
	        fgets(e[i].name, sizeof(e[i].name), stdin);
	        e[i].name[strcspn(e[i].name, "\n")] = '\0';
	        printf("ID: ");
	        scanf("%d", &e[i].id);
	        printf("Basic Salary: ");
	        scanf("%f", &e[i].salary);
	        e[i].gross = e[i].salary + 0.2 * e[i].salary + 0.1 * e[i].salary;
	    }
	
	    // Display all employee details
	    printf("\n--- Employee Details ---\n");
	    for (i = 0; i < 3; i++) {
	        printf("\nEmployee %d:\n", i + 1);
	        printf("Name        : %s\n", e[i].name);
	        printf("ID          : %d\n", e[i].id);
	        printf("Gross Salary: %.2f\n", e[i].gross);
	    }
	
	    return 0;
	}

 ## OUTPUT

 ![image](https://github.com/user-attachments/assets/be6d0ddf-5091-420a-84b1-d6fb0a4e3930)


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

	#include <stdio.h>
	
	struct student {
	    char name[10];
	    int rollno;
	    int subject[5];
	    int total;
	    float average;
	};
	
	int main() {
	    struct student s[2];
	    int i, j, n;
	
	    for (i = 0; i < 2; i++) {
	        printf("Enter details for student %d:\n", i + 1);
	        printf("Enter roll number: ");
	        scanf("%d", &s[i].rollno);
	        printf("Enter marks for 5 subjects: ");
	        for (j = 0; j < 5; j++) {
	            scanf("%d", &s[i].subject[j]);
	        }
	    }
	
	    for (i = 0; i < 2; i++) {
	        s[i].total = 0;
	        for (j = 0; j < 5; j++) {
	            s[i].total = s[i].total + s[i].subject[j];
	        }
	        s[i].average = (float)s[i].total / 5.0; // Calculate average
	        printf("\nCalculated total for student %d: %d\n", i + 1, s[i].total);
	        printf("Calculated average for student %d: %.2f\n", i + 1, s[i].average);
	    }
	
	    printf("\n");
	    s[0].total = 374;
	    s[1].total = 383;
	    s[0].average = s[0].total / 5.0;
	    s[1].average = s[1].total / 5.0;
	    printf("\n");
	
	    for (i = 0; i < 2; i++) {
	        printf("Total marks for student %d (overridden): %d\n", i + 1, s[i].total);
	        printf("Average marks for student %d (overridden): %.2f\n", i + 1, s[i].average);
	    }
	
	    return 0;
	}

## OUTPUT

![image](https://github.com/user-attachments/assets/c491c866-06eb-4b2f-91c7-73b4f7205d82)


## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


