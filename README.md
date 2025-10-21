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

Enter details of Student 1
Enter Register Number: 101
Enter mark for subject 1: 80
Enter mark for subject 2: 90
Enter mark for subject 3: 85

Enter details of Student 2
Enter Register Number: 102
Enter mark for subject 1: 75
Enter mark for subject 2: 70
Enter mark for subject 3: 80

... (similarly for 3 more students)

--------------------------------------------
RegNo   Sub1    Sub2    Sub3    Total   Average
--------------------------------------------
101     80.0    90.0    85.0    255.0   85.00
102     75.0    70.0    80.0    225.0   75.00
103     60.0    65.0    70.0    195.0   65.00
104     90.0    95.0    85.0    270.0   90.00
105     50.0    55.0    60.0    165.0   55.00


RESULT:

Thus the C program to read(rego,3 subject markss) and store the details of 5 students and calculate the Total and Average is executed successfully.












