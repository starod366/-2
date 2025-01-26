def что_надеть(температура, есть_осадки, осадки_сильные):
    if температура > 30:
        return "Легкую одежду (футболка и шорты)"
    elif 0 <= температура <= 30:
        if есть_осадки:
            if осадки_сильные:
                return "Пальто, рюкзак и зонт"
            else:
                return "Пальто и зонт"
        else:
            return "Пальто"
    else:  # температура ниже 0
        return "Пуховик"
температура = int(input("Введите температуру в градусах Цельсия: "))
есть_осадки = input("Есть осадки? (да/нет): ").strip().lower() == "да"
осадки_сильные = input("Осадки сильные? (да/нет): ").strip().lower() == "да"

одежда = что_надеть(температура, есть_осадки, осадки_сильные)    
print("Рекомендуемая одежда:", одежда)   
