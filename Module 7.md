EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

Aim:
To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

Algorithm:
1.	Declare structure eligible with age (integer) and n (character array)
2.	Declare variable e of type eligible
3.	Input age and name using scanf, store in e
4.	If e.age <= 6
-	Print "Vaccine Eligibility: No"
Else
-	Print "Vaccine Eligibility: Yes"
5.	Print details (e.age, e.n)
6.	Return 0
 
Program:

#include<stdio.h>  
  struct eligible{
  int Age;
  char name[100];
  } ;
  int main()
Output:
 Result: Thus, the program is verified successfully.
 EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND
 RETURNING A STRUCTURE FROM A FUNCTION Aim: To write a C program for passing
 structure as function and returning a structure from a function
 Algorithm:
 1. Define structure numbers with members a and b.
 2. Declare variable n of type numbers.
 3. Prompt the user to enter values for a and b.
 4. Input values for a and b into n using scanf.
 5. Call the add function with n as an argument.
 6. Print the result returned by the add function.
 7. Return 0
 Program:
```
  {
      struct eligible eli;
      scanf("%d",&eli.Age);
      printf("Age:%d\n",eli.Age);
      scanf("%s",eli.name);
      printf("Name:%svaccine:%d\n",eli.name,eli.Age);
      if(eli.Age>18)
      printf("eligibility:yes");
      else
      printf("eligibility:no");
      return 0
    }
```


Output:

![image](https://github.com/user-attachments/assets/efe07b9c-c9c3-49cf-ad40-af8b718c8c7e)



Result:
Thus, the program is verified successfully. 



EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION
Aim:
To write a C program for passing structure as function and returning a structure from a function

Algorithm:
1.	Define structure numbers with members a and b.
2.	Declare variable n of type numbers.
3.	Prompt the user to enter values for a and b.
4.	Input values for a and b into n using scanf.
5.	Call the add function with n as an argument.
6.	Print the result returned by the add function.
7.	Return 0
 
Program:
```
 #include <stdio.h>
 struct Point {
 int x;
 int y;  
};
 void displayPoint(struct Point p)
 {
 printf("Point: (%d, %d)\n", p.x, p.y);
 }
 struct Point addPoints(struct Point p1, struct Point p2) {
 struct Point result;
 result.x = p1.x + p2.x;
 result.y = p1.y + p2.y;
 return result;
 }
 int main() {
 struct Point a = {3, 4};
 struct Point b = {5, 7};
 printf("Point A: ");
 displayPoint(a);
 printf("Point B: ");
 displayPoint(b);
 struct Point sum = addPoints(a, b);
 printf("Sum of A and B: ");
 displayPoint(sum);
 return 0;
 }
```



Output:


![image](https://github.com/user-attachments/assets/4f4ef616-389e-4fb9-adad-74833ccb086f)





Result:
Thus, the program is verified successfully


 
EXP.NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()

Aim:
To write a C program to read a file name from user

Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare a character array name to store the file name.
4.	Prompt the user to enter a file name.
Use scanf to input the file name into the name array.
5.	Print a message indicating that the file with the specified name has been created successfully.
6.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
1.	Print a message indicating that the file has been opened successfully.
2.	Use fclose to close the file.
3.	Print a message indicating that the file has been closed.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:
```
 #include <stdio.h>
    int main()
    {
          FILE*file=fopen("Hospital.txt","w");
          if(file == NULL)
          {
              printf("Error creating file\n");
              return 1;
          }
          printf("File Created Successfully\n");
          printf("File Opened\n");
          fclose(file);
          printf("File Closed\n");
          return 0;
    }
```



Output:


![Screenshot 2025-04-25 225425](https://github.com/user-attachments/assets/6a5aa62f-1e70-4598-9b9e-b6e36d21607f)











Result:
Thus, the program is verified successfully
 


EXP NO:4   PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE
Aim:
To write a C program to read, a file and insert text in that file
Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare character arrays name and text. Declare an integer variable num.
4.	Prompt the user to enter a file name and the number of strings.
Use scanf to input the file name into the name array and the number of strings into the num variable.
5.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
6.	Print a message indicating that the file has been opened successfully.
1.	Use a loop to input strings from the user and write them to the file using fputs.
2.	Use fclose to close the file.
3.	Print a message indicating that data has been added successfully.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:

```
#include <stdio.h>

int main() {
    FILE *p;
    char name[100];

    printf("Enter the file name: ");
    scanf("%s", name);

    p = fopen(name, "w");

    if (p == NULL) {
        printf("Error creating file.\n");
        return 1;
    }

    printf("File '%s' created successfully.\n", name);

    fclose(p);
    printf("File closed successfully.\n");

    return 0;
}

```



Output:


![image](https://github.com/user-attachments/assets/86e6455b-fbcd-422b-8b2c-b7717aa7c2c1)







Result:
Thus, the program is verified successfully



Ex No 5 : C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE

Aim:
The aim of this program is to dynamically allocate memory to store information about multiple subjects (name and marks), input the details for each subject, and then display the stored information. Finally, it frees the allocated memory to prevent memory leaks.

Algorithm:
1.Input the number of subjects.

2.Read the integer value n from the user, which represents the number of subjects.

3.Dynamically allocate memory:

4.Use malloc to allocate memory for n subjects. Each subject has a name (array of characters) and marks (integer).

5.If memory allocation fails (i.e., the pointer s is NULL), display an error message and exit the program.

6.Input the details of each subject

7.Use a for loop to read the name and marks of each subject using scanf. For each subject, store the name as a string and marks as an integer in the dynamically allocated memory.

8.Display the details of each subject

9.Use another for loop to print the name and marks of each subject.

10.Free the allocated memory

11.After all operations are done, call free(s) to release the dynamically allocated memory.

12.Return from the main function

13.End the program by returning 0.

Program:

```
#include <stdio.h>
struct Student {
    char name[50];
    int roll;
    float marks;
};

int main() {
    struct Student s;
    printf("Enter student name: ");
    fgets(s.name, sizeof(s.name), stdin);

    printf("Enter roll number: ");
    scanf("%d", &s.roll);

    printf("Enter marks: ");
    scanf("%f", &s.marks);
    printf("\n--- Student Details ---\n");
    printf("Name       : %s", s.name);
    printf("Roll No.   : %d\n", s.roll);
    printf("Marks      : %.2f\n", s.marks);

    return 0;
}
```




Output:


![image](https://github.com/user-attachments/assets/d1f6ccb0-b742-47e3-b313-9ea9afac3e1e)







Result:
Thus, the program is verified successfully
