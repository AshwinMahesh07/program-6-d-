# program-6-d-
C module 6
EXP.No:6-d-Total and average of marks using structure.

Date:19/10/2025

Name: VASANTH S

Ref no: 25017538

AIM:
Create a structure program to read(rego,3 subject markss) and store the details of 5 students and calculate the Total and Average

ALGORITHM:


Define a structure Student with members:
	•	regno (integer)
	•	marks[3] (array for 3 subject marks)
	•	total and average (float)
Declare an array of 5 Student structures.
For each student:
	•	Read register number and marks for 3 subjects.
	•	Calculate total = sum of marks.
	•	Calculate average = total / 3.
Display each student’s details, total, and average.



PROGRAM:

```
#include <stdio.h>

struct Student {
    int regno;
    float marks[3];
    float total;
    float average;
};

int main() {
    struct Student s[5];
    int i, j;

    // Read details of 5 students
    for (i = 0; i < 5; i++) {
        printf("\nEnter details of Student %d\n", i + 1);
        printf("Enter Register Number: ");
        scanf("%d", &s[i].regno);

        s[i].total = 0;
        for (j = 0; j < 3; j++) {
            printf("Enter mark for subject %d: ", j + 1);
            scanf("%f", &s[i].marks[j]);
            s[i].total += s[i].marks[j];
        }

        s[i].average = s[i].total / 3.0;
    }

    // Display results
    printf("\n--------------------------------------------\n");
    printf("RegNo\tSub1\tSub2\tSub3\tTotal\tAverage\n");
    printf("--------------------------------------------\n");

    for (i = 0; i < 5; i++) {
        printf("%d\t", s[i].regno);
        for (j = 0; j < 3; j++) {
            printf("%.1f\t", s[i].marks[j]);
        }
        printf("%.1f\t%.2f\n", s[i].total, s[i].average);
    }

    return 0;
}
```

OUTPUT:


<img width="392" height="639" alt="Screenshot 2025-10-21 at 9 06 01 AM" src="https://github.com/user-attachments/assets/06557317-3520-4c20-906f-16ab2bd3ffa5" />


RESULT:

Thus the C program to read(rego,3 subject markss) and store the details of 5 students and calculate the Total and Average is executed successfully.












