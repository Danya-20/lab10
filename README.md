# lab10
2.2 Мета роботи:
Метою цієї лабораторної роботи є ознайомлення з основними принципами об'єктно-орієнтованого програмування (ООП), такими як інкапсуляція, наслідування, поліморфізм, та створення класів та об'єктів на мові програмування Python.

2.3 Опис завдання:
Створення класу Student:

Написати клас Student з атрибутами name, age та grade.
Створення методу для класу Student:

Додати метод display_info, який повертає інформацію про студента у вигляді рядка.
Наслідування:

Створити базовий клас Animal з атрибутами name та sound, та методом make_sound.
Створити похідний клас Dog, який наслідує Animal та додає атрибут breed.
Поліморфізм:

Створити базовий клас Bird з методом fly.
Створити два похідних класи Sparrow та Penguin, які перевизначають метод fly.
Інкапсуляція:

Створити клас Encapsulation з публічним, приватним та захищеним атрибутами.
Створення класу Rectangle:

Написати клас Rectangle з атрибутами width та height, та методом calculate_perimeter, який обчислює периметр прямокутника.
Створення класу AverageCalculator:

Написати клас AverageCalculator з атрибутом numbers, який є списком чисел, та методом calculate_average, який обчислює середнє значення чисел.
2.4 Виконання роботи:
Клас Student:

class Student:
    def __init__(self, name, age, grade):
        self.name = name
        self.age = age
        self.grade = grade

    def display_info(self):
        return f"Name: {self.name}, Age: {self.age}, Grade: {self.grade}"
Наслідування Animal та Dog:


class Animal:
    def __init__(self, name, sound):
        self.name = name
        self.sound = sound

    def make_sound(self):
        return f"{self.name}: {self.sound}"

class Dog(Animal):
    def __init__(self, name, sound, breed):
        super().__init__(name, sound)
        self.breed = breed
Поліморфізм Bird, Sparrow, та Penguin:


class Bird:
    def fly(self):
        return None

class Sparrow(Bird):
    def fly(self):
        return "Sparrow flies high"

class Penguin(Bird):
    def fly(self):
        return "Penguin cannot fly"
Інкапсуляція Encapsulation:

class Encapsulation:
    def __init__(self, public, private, protected):
        self.public = public
        self._private = private
        self.__protected = protected
Клас Rectangle:

class Rectangle:
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def calculate_perimeter(self):
        return 2 * (self.width + self.height)
Клас AverageCalculator:


class AverageCalculator:
    def __init__(self, numbers):
        self.numbers = numbers

    def calculate_average(self):
        return sum(self.numbers) / len(self.numbers)
2.5 Результати:
Було створено та протестовано класи згідно завдань. Нижче наведено приклади використання створених класів та методів:


# Task 1 & 2
student = Student("Alice", 20, "A")
print(student.display_info())  # Output: Name: Alice, Age: 20, Grade: A

# Task 3
dog = Dog("Buddy", "Woof", "Golden Retriever")
print(dog.make_sound())  # Output: Buddy: Woof

# Task 4
sparrow = Sparrow()
penguin = Penguin()
print(sparrow.fly())  # Output: Sparrow flies high
print(penguin.fly())  # Output: Penguin cannot fly

# Task 5
encapsulation = Encapsulation("public_value", "private_value", "protected_value")
print(encapsulation.public)  # Output: public_value
# print(encapsulation._private)  # Not recommended to access directly
# print(encapsulation.__protected)  # Will raise an AttributeError

# Task 6
rectangle = Rectangle(4, 7)
print(rectangle.calculate_perimeter())  # Output: 22

# Task 7
average_calculator = AverageCalculator([1, 2, 3, 4, 5])
print(average_calculator.calculate_average())  # Output: 3.0
