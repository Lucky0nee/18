#include <iostream>
#include <array>

using namespace std;

int main() {
	setlocale(LC_CTYPE, "ukr");
	array <int, 10> arr{ 3000, 1000, 500, 200, 100, 50, 25, 10, 5, 1 };
	array <int, 10> sum{ 0,       0,  0,   0,    0,  0,  0, 0, 0, 0 };
	int limit = 40;
	long long int money, temp;
	cout << "\t\t\t\t\t\t------" << "Банк" << "------\n";
	cout << "Скiльки ви хочете зняти?\n";
	cin >> money; temp = money;
	system("cls");
	//cout << "\t\t\t\t\t\t------" << money << "------\n";
x:
	if (money == 0 || limit <= 0) {
		goto end;
	}

	for (int i = 0; i < arr.size(); i++) {
		if (money == arr[i]) {
			//cout << limit << ". " << money; // Test
			money -= arr[i];
			sum[i]++; limit--;
		}
	}
	for (int i = 0; i < arr.size(); i++) {
		for (int j = 0; j < arr.size(); j++) {
			for (int h = 0; h < arr.size(); h++) {
				if (money > arr[h]) {
					money -= arr[h];
					//cout << limit << ". " << arr[h] << "\n";  // Test
					sum[h]++; limit--;
					goto x;
				}
			}
		}
	}
	//system("cls");
end:
	if (limit <= 0) {
		cout << "\nЧерез лiмiт видано лише: 120000\n";
	}
	else {
		cout << "\t\t\t\t\t\t------" << temp << "------\n";
	}

	for (int i = 0; i < arr.size(); i++) {
		cout << arr[i] << " - "; cout << sum[i] << "\n";
	}
}
/*
Національний банк (версія 2.0 :) випустить банкноти номіналом 3000, 1000, 500,
200, 100, 50, 25, 10, 5 та 1.
Ваше завдання — написати програму для банкоматів, яка має знайти мінімальну
кількість банкнот для видачі будь-якої суми клієнтам.
Майбутній міністр фінансів України попросив, щоб ваш код видав на екран
значення і кількість всіх типів банкнот окремо для вказаної суми.
Також врахуйте той факт, що банкомати Вінкор-ніксдорф можуть видавати за
один раз не більше 40 банкнот.
*/
