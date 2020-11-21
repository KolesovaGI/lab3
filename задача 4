#include <stdio.h>
#include <stdlib.h>
#include <time.h>
#include <conio.h>

#define size 10

int maximum(int a[]);
int minimum(int a[]);
float middle(int a[]);
int mediana(int a[]);

int main(void)
{
    int a[size];

    srand(time(NULL));

    for (int i = 0; i < size; i++)
    {
        a[i] = rand() % 100;
        printf("%d ", a[i]);
    }

    FILE* task_three; 
    task_three = fopen("C:\\Users\\1\\Desktop\\homeworks\\task_three.txt", "r");

    if (task_three == 0)
    {
        printf("Error");
    }

    else
    {

        for (int i = 0; i < size; i++)
        {
            fscanf(task_three, "%d", &a[i]);
        }

        fclose(task_three);
    }


    task_three = fopen("C:\\Users\\1\\Desktop\\homeworks\\task_three.txt", "a");

    fprintf(task_three, "Maximal number in the array = %d\n", maximum(a));
    fprintf(task_three, "Minimal number in the array = %d\n", minimum(a));
    fprintf(task_three, "Middle number in the array = %.1f\n", middle(a));
    fprintf(task_three, "Median of the array = %d\n", mediana(a));

    fclose(task_three);
}

int minimum(int a[])
{
    int min = a[0];

    for (int i = 1; i < size; i++)
    {
        if (a[i] < min)
        {
            min = a[i];
        }
    }

    return min;
}

int maximum(int a[])
{
    int max = a[0];

    for (int i = 1; i < size; i++)
    {
        if (a[i] > max)
        {
            max = a[i];
        }
    }

    return max;
}

float middle(int a[])
{
    double middle = 0;

    for (int i = 0; i < size; i++)
    {
        middle += a[i];
    }

    return middle / size;
}

int mediana(int a[])
{
    for (int i = 0; i < size - 1; i++)
    {
        for (int i = 0; i < size - i - 1; i++)
        {
            if (a[i] > a[i + 1])
            {
                a[i] = a[i] + a[i + 1];
                a[i + 1] = a[i] - a[i + 1];
                a[i] = a[i] - a[i + 1];
            }
        }
    }

    if (size % 2 != 0)
    {
        return a[size / 2];
    }

    else
    {
        return (a[size / 2] + a[size / 2 - 1]) / 2;
    }
}
