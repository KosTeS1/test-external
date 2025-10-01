# Задание 1

Дана переменная, в которой хранится четырёхзначное число (год). Нужно написать программу, которая выведет, является этот год високосным или обычным.

def check_year(year):
    # Компактная версия с одним условием
    if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
        result = 'Високосный год'
    else:
        result = 'Обычный год'
    
    return result

if __name__ == '__main__':
    year_result = check_year(2024)
    assert year_result == 'Високосный год', "Ответ должен быть Високосный год"
    print(f"2024 какой год: {year_result}")
    
    year_result = check_year(2025)
    assert year_result == 'Обычный год', "Ответ должен быть Обычный год"
    print(f"2025 какой год: {year_result}")