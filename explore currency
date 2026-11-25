#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main()
{
    int choice, difficulty;
    int a, b, answer, correctAnswer;
    int score = 0;
    int totalQuestions = 10;
    int i;

    srand(time(NULL));

    printf("\n====================================\n");
    printf("       MATH CHALLENGE GAME\n");
    printf("====================================\n");

    printf("\nSelect Difficulty Level:\n");
    printf("1. Easy\n");
    printf("2. Medium\n");
    printf("3. Hard\n");

    printf("\nEnter your choice: ");
    scanf("%d", &difficulty);

    printf("\nGame Started! Answer the questions.\n");

    for (i = 1; i <= totalQuestions; i++)
    {
        if (difficulty == 1)
        {
            a = rand() % 10 + 1;
            b = rand() % 10 + 1;
        }
        else if (difficulty == 2)
        {
            a = rand() % 50 + 1;
            b = rand() % 50 + 1;
        }
        else if (difficulty == 3)
        {
            a = rand() % 100 + 1;
            b = rand() % 100 + 1;
        }
        else
        {
            printf("Invalid difficulty!\n");
            return 0;
        }

        choice = rand() % 4 + 1;

        printf("\n------------------------------------\n");
        printf("Question %d of %d\n", i, totalQuestions);

        switch (choice)
        {
            case 1:
                correctAnswer = a + b;
                printf("%d + %d = ", a, b);
                break;

            case 2:
                if (a < b)
                {
                    int temp = a;
                    a = b;
                    b = temp;
                }
                correctAnswer = a - b;
                printf("%d - %d = ", a, b);
                break;

            case 3:
                correctAnswer = a * b;
                printf("%d x %d = ", a, b);
                break;

            case 4:
                correctAnswer = a;
                b = (rand() % 10) + 1;
                a = a * b;
                printf("%d / %d = ", a, b);
                break;
        }

        if (scanf("%d", &answer) != 1)
        {
            printf("Invalid input! Game ended.\n");
            return 0;
        }

        if (answer == correctAnswer)
        {
            printf("Correct Answer! Great Job!\n");
            score += 10;
        }
        else
        {
            printf("Wrong Answer!\n");
            printf("Correct Answer: %d\n", correctAnswer);
        }

        printf("Current Score: %d\n", score);
    }

    printf("\n====================================\n");
    printf("          GAME OVER!\n");
    printf("====================================\n");

    printf("Total Questions : %d\n", totalQuestions);
    printf("Correct Score   : %d / 100\n", score);
    printf("Percentage      : %d%%\n", score);

    if (score == 100)
        printf("Excellent! You are a Math Champion!\n");
    else if (score >= 70)
        printf("Very Good! Keep it up!\n");
    else if (score >= 40)
        printf("Good Try! Practice more!\n");
    else
        printf("Keep Practicing! You can do better!\n");

    printf("\nThanks for Playing!\n");

    return 0;
}
