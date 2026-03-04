# needmorefood

Псевдокод:

```
ПРОГРАММА "Пора покушать"

    ГЛАВНЫЙ МЕТОД:
        СОЗДАТЬ объект food типа Food
        СОЗДАТЬ объект selectable типа Food (но ссылка типа Selectable)
        
        ВЫЗВАТЬ метод callFoodMethods с параметром food
        ВЫЗВАТЬ метод callSelectableMethods с параметром selectable
    
    МЕТОД callFoodMethods (принимает Food food):
        // Для переменной food доступны оба метода
        ВЫЗВАТЬ food.onEat()
        ВЫЗВАТЬ food.onSelect()
    
    МЕТОД callSelectableMethods (принимает Selectable selectable):
        // Для переменной selectable доступен только метод интерфейса
        ВЫЗВАТЬ selectable.onSelect()
    
    ИНТЕРФЕЙС Selectable:
        ОБЪЯВИТЬ метод onSelect()
    
    КЛАСС Food РЕАЛИЗУЕТ интерфейс Selectable:
        МЕТОД onSelect():
            ВЫВЕСТИ "The food was selected"
        
        МЕТОД onEat():
            ВЫВЕСТИ "The food was eaten"

КОНЕЦ ПРОГРАММЫ
```

Что происходит в программе:

1. Создаются два объекта Food, но с разными типами ссылок
2. Для food (тип Food) доступны оба метода - onEat() и onSelect()
3. Для selectable (тип Selectable) доступен только метод onSelect()
4. Вызов методов демонстрирует полиморфизм - даже через ссылку интерфейса вызывается реализация класса Food



Давай напишем программу, которая поможет тебе выбрать, что съесть на обед.
Для этого нужно:

Реализовать интерфейс Selectable в классе Food.
Метод onSelect() должен выводить на экран фразу "The food was selected".
Подумай, какие методы можно вызвать для переменной food, а какие для — selectable.
В методе callFoodMethods вызови методы onSelect, onEat, если это возможно.
В методе callSelectableMethods вызови методы onSelect, onEat, если это возможно.
Не используй явное приведение типов.
