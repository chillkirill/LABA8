# Ввод данных: осадки и температура для каждого дня месяца
precipitation = list(map(float, input("Введите количество осадков (мм) для каждого дня месяца через пробел: ").split()))
temperature = list(map(float, input("Введите температуру воздуха (°C) для каждого дня месяца через пробел: ").split()))

# Инициализация переменных для суммы осадков снега и дождя
snow_precipitation = 0
rain_precipitation = 0

# Пробегаем по дням и вычисляем сумму осадков снега и дождя
for i in range(len(precipitation)):
    if temperature[i] <= 0:  # Если температура ниже или равна 0, то осадки - снег
        snow_precipitation += precipitation[i]
    else:  # Если температура выше 0, то осадки - дождь
        rain_precipitation += precipitation[i]

# Вывод результатов
print(f"Общее количество осадков в виде снега: {snow_precipitation} мм")
print(f"Общее количество осадков в виде дождя: {rain_precipitation} мм")
