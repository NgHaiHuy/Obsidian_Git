```c
// Chương trình quản lý điểm sinh viên
#include <stdio.h>

struct Student {
	int student_id;
	float student_score;
};

void inputStudentInformation(struct Student s[50], int *n);
void displayScore(struct Student s[50], int n);

void findStudent();
void scoreStatistics();

int main() {
	
	struct Student s[50];
	int n = 0;
	int choice;
	
	do {
		printf("\n---- Score Management System ----\n");
		printf("1. Enter information.\n");
		printf("2. Display List.\n");
		printf("3. Rank Score (Low to hight).\n");
		printf("4. Rank Score (Hight to low).\n");
		printf("5. Find Student.\n");
		printf("6. Statistical.\n");
		printf("7. Exit.\n");
		
		printf("Enter your choice: ");
		while (scanf("%d", &choice) != 1) {
            printf("Invalid input. Please enter a number (1-7): ");
        }
		
		switch (choice) {
			case 1:
				inputStudentInformation(s, &n);
				break;
			case 2:
				displayScore(s, n);
				break;
			case 3:
				
				break;
			case 4:
				
				break;
			case 5:
				
				break;
			case 6:
				
				break;
			case 7:
				printf("\nExit program...\n");
				break;
			default:
				printf("Invalid choice! Please try again.");
		}
		
	} while (choice != 7);
	
	return 0;
}

void inputStudentInformation(struct Student s[50], int *n) {
	
	printf("Enter the number of students(Max 50 students): ");
	scanf("%d", &n);
	
	for(int i = 1; i <= n; i++) {
		printf("\nEnter student information %d.\n", i);
		
		printf("Enter student ID: ");
		scanf("%s", &s[i].student_id);
					
		printf("Enter student score: ");
		scanf("%1f", &s[i].student_score);
		getchar();
		
		printf("\n");
	}
	
}

void displayScore(struct Student s[50], int n) {
	if (n == 0) {
		printf("No student to display!\n");
		return;
	}
	
	printf("\n----- Student List -----\n");
	for(int i = 1; i <= n; i++) {
		printf("%d. Student ID: %s - Score: %1f \n", i, s[i].student_id, s[i].student_score);
	}
	
}




