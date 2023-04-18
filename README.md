#include <stdio.h>

int main() {
    const float pay_increase = 0.076; // 7.6% pay increase
    float current_salary, retroactive_pay, newAnnual_salary, newMonthly_salary;

    while (1) {
        printf("Enter current annual salary (enter 0 to stop): ");
        scanf("%f", &current_salary);

        if (current_salary == 0) {
            break;
        }

        retroactive_pay = (current_salary * pay_increase) / 2; // retroactive pay for 6 months
        newAnnual_salary = current_salary * (1 + pay_increase);
        newMonthly_salary = newAnnual_salary / 12.0;

        printf("Retroactive pay due: $%.2f\n", retroactive_pay);
        printf("New annual salary: $%.2f\n", newAnnual_salary);
        printf("New monthly salary: $%.2f\n\n", newMonthly_salary);
    }

    return 0;
}
