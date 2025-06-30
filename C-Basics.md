# Module 1

## 1
In the peaceful town of Edunova, every student's academic record is maintained by an old wise owl named Professor Quill. He records student names, roll numbers, and their subject scores with utmost care in the Great Ledger of Learning. One day, you're appointed as Professor Quill's assistant, and your task is to correctly transcribe the details of a student into the record for future reference. You are given the student's name, roll number, and the marks secured in four different subjects. Help Professor Quill by neatly printing this data in the order it should appear in the ledger.
### Input Format
The first line contains a string name representing the name of the student.
The second line contains an integer roll representing the roll number of the student.
The next four lines each contain an integer representing the marks obtained in four different subjects.
### Output Format
Print the student's name in the format: Name: <name>
Print the student's roll number in the format: RollNo: <roll>
Print the marks obtained in each of the four subjects in the format: Marks: <marks>.

```C
#include<stdio.h>
#include<string.h>

void main()
{
    char name[100];
    int rollNo,m1,m2,m3,m4;
    
    scanf("%[^\n] %d %d %d %d %d", name, &rollNo, &m1, &m2, &m3, &m4);
        
    if (strlen(name) <= 100){    
        printf("Name: %s\n", name);
    }
    

    if((rollNo >= 1) && (rollNo <= 1000)){
        printf("RollNo: %d\n", rollNo);
    }
    
    
    if ((m1 <=100) && (m2 <=100) && (m3 <=100) && (m4 <=100)){
        printf("Marks: %d %d %d %d\n", m1,m2,m3,m4);
    }
}

```



