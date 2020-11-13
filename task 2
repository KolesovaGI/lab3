#include <stdio.h>
#include <stdlib.h>
#include <time.h>
#define size 20
 
int main() 
{
  int nums[size];
  int i, j, b;

  srand(time(NULL));

  for (i = 0; i < size; i++) 
  {
    nums[i] = rand() % 100;
    printf("%3d", nums[i]);
  }
  printf("\n");

  for (i = 0; i < size - 1; i++) 
  {
    for (j = 0; j < size - i - 1; j++) 
    {
      if (nums[j] > nums[j + 1]) 
      {
        b = nums[j];
        nums[j] = nums[j + 1];
        nums[j + 1] = b;
      }
    }
  }

  for (i = 0; i < size; i++)
  {
    printf("%3d", nums[i]);
  }

  printf("\n");
}
