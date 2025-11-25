# telephone-directory
c program to create telephone directory
#include <stdio.h>
#include <string.h>
int main() {
    int n, i, found = 0;
    char names[50][50], disease[50][50], search[50];
    printf("Enter number of patients: ");
    scanf("%d", &n);
    // Input patient details
    for(i = 0; i < n; i++) {
        printf("\nEnter name of patient %d: ", i + 1);
        scanf("%s", names[i]);
        printf("Enter disease of %s: ", names[i]);
        scanf("%s", disease[i]);
    }
    // Search patient
    printf("\nEnter patient name to search: ");
    scanf("%s", search);
    for(i = 0; i < n; i++) {
        if(strcmp(names[i], search) == 0) {
            found = 1;
            printf("\n--- Patient Record Found ---\n");
            printf("Name    : %s\n", names[i]);
            printf("Disease : %s\n", disease[i]);
            break;
        }
    }
    if(!found) {
        printf("\nRecord not found.\n");
    }
    return 0;
}
