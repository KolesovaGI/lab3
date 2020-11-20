#include <stdio.h>
#include <stdlib.h>
#include <time.h>

#define size 10

void sift_down(int *numbers, int root, int bottom);
void heap_sort(int *numbers, int array_size);

int main ()
{
  int a[size];

  srand(time(NULL));

  for (int i = 0; i < size; i++)
  {
    a[i] = rand() % 100;
  }

  for (int i = 0; i < size; i++)
  {
    printf("%d ", a[i]);
  }

  printf("\n");

  heap_sort(a, 10);

  for (int i = 0;  i< size; i++)
  {
    printf("%d ", a[i]);
  }

  printf("\n");

  return 0;
}

void sift_down(int *numbers, int root, int bottom)
{
  int max_child;
  int done = 0;

  while ((root * 2 <= bottom) && (!done))
  {
    if (root * 2 == bottom)
    {
      max_child = root * 2;
    }

    else if (numbers[root * 2] > numbers[root * 2 + 1])
    {
      max_child = root * 2;
    }

    else
    {
      max_child = root * 2 + 1;
    }

    if (numbers[root] < numbers[max_child])
    {
      int temp = numbers[root];

      numbers[root] = numbers[max_child];
      numbers[max_child] = temp;
      root = max_child;
    }

    else
    {
      done = 1;
    }
  }
}

void heap_sort(int *numbers, int array_size)
{
  for (int i = (array_size / 2) - 1; i >= 0; i--)
  {
    sift_down (numbers, i, array_size - 1);
  }

  for (int i = array_size - 1; i >= 1; i--)
  {
    int temp = numbers[0];

    numbers[0] = numbers[i];
    numbers[i] = temp;
    sift_down(numbers, 0, i - 1);
  }
}
