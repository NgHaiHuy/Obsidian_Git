```c
// Chương trình quản lý điểm sinh viên
#include <stdio.h>
#include <stdbool.h>

struct Student {
	int student_id;
	float student_score;
};

void inputStudentInformation(struct Student s[50], int *n);
void displayScore(struct Student s[50], int n);

void rankScoreLowToHigh(struct Student s[50], int n);
void rankScoreHighToLow(struct Student s[50], int n);

void findStudent(struct Student s[50], int n);
void scoreStatistics(struct Student s[50], int n);

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
				rankScoreLowToHigh(s, n);
				break;
			case 4:
				rankScoreHighToLow(s, n);
				break;
			case 5:
				findStudent(s, n);
				break;
			case 6:
				scoreStatistics(s, n);
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
	scanf("%d", n);
	
	for(int i = 1; i <= *n; i++) {
		printf("\nEnter student information %d.\n", i);
		
		printf("Enter student ID: ");
		scanf("%d", &s[i].student_id);
					
		printf("Enter student score: ");
		scanf("%f", &s[i].student_score);
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
		printf("%d. Student ID: %d - Score: %.2f \n", i, s[i].student_id, s[i].student_score);
	}
	
}

// (seclection sort)
void rankScoreLowToHigh(struct Student s[50], int n) {
	if (n == 0) {
		printf("No student to display!\n");
		return;
	}
	
	int min;
    struct Student temp;
    
    for(int i = 1; i < n; i++) {
        min = i;
        
        for(int j = i + 1; j <= n; j++) {
            if (s[j].student_score < s[min].student_score) {
                min = j;
            }
        }
        
        temp = s[i];
        s[i] = s[min];
        s[min] = temp;
    }
    
    printf("\n--- Rank score low to high ---\n");
    
    for(int i = 1; i <= n; i++) {
        printf("%d. Id: %d - Score: %.2f\n", i, s[i].student_id, s[i].student_score);
    }
}

// (bubble sort)
void rankScoreHighToLow(struct Student s[50], int n) {
	if (n == 0) {
		printf("No student to display!\n");
		return;
	}
	
	bool swapped;
	struct Student temp;
	
	for(int i = 1; i <= n; i++) {
		swapped = false;
		
		for(int j = 1; j <= n - i; j++) {
			if(s[j].student_score < s[j+1].student_score) {
				
				temp = s[j];
                s[j] = s[j + 1];
                s[j + 1] = temp;
                swapped = true;
			}
		}
		
		if (!swapped)
			break;
	}
	
    printf("\n--- Rank score high to low ---\n");
	
    for(int i = 1; i <= n; i++) {
        printf("%d. Id: %d - Score: %.2f\n", i, s[i].student_id, s[i].student_score);
    }
	
}

void findStudent(struct Student s[50], int n) {
	if (n == 0) {
		printf("No student to display!\n");
		return;
	}
	
	int x; 
	
	printf("\nEnter student ID to find: ");
	scanf("%d", &x);
	
	for(int i = 0; i <= n; i++) {
		if(s[i].student_id == x) {
			printf("\nStudent ID %d have score = %.2f\n", s[i].student_id, s[i].student_score);
		}
	}
	
}

void scoreStatistics(struct Student s[50], int n) {
	if (n == 0) {
		printf("No student to analyze!\n");
		return;
	}
	
	float sum = 0;
	float maxScore = s[1].student_score;
	float minScore = s[1].student_score;
	
    for(int i = 1; i <= n; i++) {
        sum += s[i].student_score;
        
        if(s[i].student_score > maxScore) {
            maxScore = s[i].student_score;
        }
        
        if(s[i].student_score < minScore) {
            minScore = s[i].student_score;
        }
    }
	
	float average = sum / n;
	
	printf("\n--- Score statistics ---\n");
	
	printf("Average score is: %.2f\n", average);
	
	printf("Highest score is: %.2f\n", maxScore);
	
	printf("Lowest score is: %.2f\n", minScore);
	
}
