# Module 1
## Workouts
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

## 2

In the quiet corners of the library, two friends are engrossed in a project that demands precise calculations. While one scribbles ideas, the other wrestles with two numbers one in each hand. The task seems simple: combine them to discover their power when multiplied, and then understand how one divides the other. The results could shape the outcome of their project. But if a mistake sneaks in a letter instead of a digit the whole equation collapses. Accuracy is everything in this mathematical duet.

## Input Format
The first line of input contains an integer a.
The second line of input contains an integer b.
## Output Format
Print the product of the two integers.
• Print the quotient when a is divided by b.
Print Invalid input if the input contains characters.

```C
#include<stdio.h>
#include<math.h>

void main()
{
    int a,b;
    
    if (scanf("%d %d", &a,&b) == 2){
        if ((a >= -1000 && a <= 1000) && (b >= -1000 && b <= 1000)){
            if (b != 0){
                printf("%d\n", a * b);
                printf("%d\n", a/b);
            }
               
        }
    }
    
    else{
        printf("Invalid input\n");
    }
    
}
```


## 3
In a computer science class, the instructor wants to honor the legendary computer scientist Dennis Ritchie, who co-created the C programming language. To commemorate his contributions to the field, the instructor has decided to display his name on the screen during the lecture. Help the instructor to implement a simple program to print.

## Input Format
Not applicable, as this program does not require any input from the user.
## Output Format
Print the string "Dennis Ritchie".

```C
#include<stdio.h>

void main(){
    
    char c[10];
    
    if (scanf("%s", c)){
        printf("Dennis Ritchie\n");
    }
}
```

## 4

In a geometry lab activity, students are investigating triangle angle relationships. Given two known angles of a triangle, help them determine the third angle, ensuring the input values are valid and form a proper triangle.
## Input Format
Two space-separated integers representing the first and second angles.
## Output Format
Print the third angle of the triangle.
Print "Invalid input" if either angle is negative or if their sum exceeds 180.
```C
#include<stdio.h>

void main(){
    int a,b,c;
    scanf("%d %d", &a, &b);
    c = 180 - (a+b);
    if ((a >= 0 && b <= 180) && (c)){
        printf("%d",  c);
    }
    
    else{
        printf("Invalid input");
    }
    
    
}

```

## 5 

At a civic awareness camp, participants check if they're ready for their first vote. A validation system reviews each person's age and responds with encouragement or approval based on eligibility.
## Input Format
A single integer representing the age.
## Output Format
Print "Eligible" if age is 18 or above.
Print "Not eligible" if age is below 18.
Print "Invalid input" if the age is negative.

```C
#include<stdio.h>

void main(){
    
    int age;
    scanf("%d", &age);
    
    if (age >= -10 && age <= 120){
        if (age >= 18){
            printf("Eligible");
        }else{
            printf("Not eligible");
        }
    }else{
        printf("Invalid input");
    }
    
}
```


## 6

In the enchanted village of Mirrovia, two magical numbers are displayed side by side on a glowing scroll. These numbers often need to swap places for a balance spell to work properly. You are the royal programmer, tasked with ensuring the scroll always reflects the swapped state of these numbers.Given two integers, your mission is to switch their positions using a spell of precision and display the result in the sacred format the scroll understands.
## Input Format
The first line contains an integer a representing the first magical number.
The second line contains an integer b representing the second magical number.
## Output Format
Print the output in the following format: Swapped values : <value_of_a>,<value_of_b>

```C
#include<stdio.h>


void main()
{
    
    int a,b,t;
    scanf("%d %d", &a, &b);
    
    t = a;
    a = b;
    b = t;
    
    printf("Swapped values  : %d,%d", a, b);
}
```

## 7
As a health advisor, calculate Body Mass Index (BMI) to assess whether an individual has a healthy body weight for their height. The BMI is determined using the following formula:
BMI = weight * height2

## Input Format

The first line consists of one integer representing weight (in kilograms).
The second line consists of one floating-point number representing height (in meters).

## Output Format
Print the BMI rounded off to two precision points.

```C
#include<stdio.h>

void main()
{
    int kg;
    float h;
    
    scanf("%d %f", &kg, &h);
    
    if ((kg >= 0 && kg <=100) && (h >= 0.0 && h <=5.5)){
        float h2 = h*h;
        
        float bmi = (float) kg / h2;
        printf("%.2f\n", bmi );
    }
}
```

## 8

Chef Alex is preparing a special dish and needs to measure precise quantities of flour and sugar for his recipe. Help him by implementing a module that reads two integers: one for the quantity of flour and another for sugar, then display the quantities of flour and sugar.
## Input Format
The first integer represents the quantity of flour, denoted as 'a'.
The second integer represents the quantity of sugar, denoted as 'b'.
## Output Format
Print the two integers in the format:

Flour: <a>
Sugar: <b>.

```C
#include<stdio.h>

void main()
{
    int a,b;
    scanf("%d %d", &a,&b);
    if (a>=1||b <= 100){
    printf("Flour: %d\n", a);
    printf("Sugar: %d\n",b);}

    
}

```

## 9
A vigilant traffic officer stands at an intersection, keenly observing the colorful signals of the traffic lights. Intrigued by their meanings, they decide to implement a module to decipher the signals and ensure safety on the roads. Your task is to create a program that reads the traffic light signal and prints the corresponding action.
When the traffic light shows Red, it commands Stop.
• When it displays Yellow, it prompts Ready.
When it gleams Green, it eagerly shouts Go.
## Input Format
The input consists of a string s representing the traffic light signal.
## Output Format:
Print the corresponding action based on the signal.
Print "Invalid input" for any other color.

```C
#include<stdio.h>
#include<string.h>

int main()
{
    char txt[100];
    scanf("%[^/]", txt);
        // printf("%s", txt);

    if (strcmp(txt,"Red") == 0){
        printf("Stop\n");
    }
    
    else if (strcmp(txt,"Yellow") == 0){
        printf("Ready\n");
    }
    
    else if (strcmp(txt,"Green") == 0){
        printf("Go\n");
    }
    
    else{
        printf("Invalid input\n");
        
    }
    
    return 0;
    
}
```

## 10

Ms. Edwards's class uses an interactive app to teach students about vowels and consonants. Students enter a single letter, and the app instantly tells them whether the letter is a vowel or a consonant. If the input is not a valid alphabet letter, the app will display an error message.
## Input Format
The input consists of a single character, ch
## Output Format

Print Vowel if the character is a vowel (a, e, i, o, u - case-insensitive).
Print Consonant if the character is a consonant (any other alphabetic character).
Print Invalid input if the input is not an alphabetic character.

```C
#include<stdio.h>
#include<ctype.h>

int main()
{
    char ch;
    
    scanf("%c", &ch);
    
        
    if(!isalpha(ch)){
        printf("Invalid input");
        return 0;
        
    }
    
    if (ch == 'a' || ch == 'A' || ch == 'e' || ch == 'E' || ch == 'i' || ch == 'I'  || ch == 'o' || ch == 'O' || ch == 'u' || ch == 'U'  ){
        printf("Vowel\n");
    }

    
    else if(!(ch == 'a' || ch == 'A' || ch == 'e' || ch == 'E' || ch == 'i' || ch == 'I'  || ch == 'o' || ch == 'O' || ch == 'u' || ch == 'U'  )){
        printf("Consonant\n");
    }
    return 0;
    
}
```
