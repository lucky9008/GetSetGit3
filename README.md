# GetSetGit3
int #include <stdio.h>

int main() {
    int *num1, *num2, *result;
    int i, n;
    printf("Enter the number of pairs of numbers to multiply: ");
    scanf("%d", &n);
    num1 = (int*)malloc(n * sizeof(int));
    num2 = (int*)malloc(n * sizeof(int));
    result = (int*)malloc(n * sizeof(int));
   printf("Enter the numbers:\n");
    for (i = 0; i < n; i++) {
        printf("Enter number %d: ", i + 1);
        scanf("%d", &num1[i]);
        printf("Enter number %d: ", i + 1);
        scanf("%d", &num2[i]);
    }
    for (i = 0; i < n; i++) {
        result[i] = *(num1 + i) * *(num2 + i);
    }

  printf("\nResults:\n");
    for (i = 0; i < n; i++) {
        printf("%d * %d = %d\n", num1[i], num2[i], result[i]);
    }
    free(num1);
    free(num2);
    free(result);
    return 0;
}
