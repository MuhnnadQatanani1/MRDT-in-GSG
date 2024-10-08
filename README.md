## Object-Oriented Programming (OOP) in this Project

This project follows the principles of **Object-Oriented Programming (OOP)**, which is a programming paradigm based on the concept of "objects." These objects can contain both data (attributes) and code (methods), making it easier to structure and manage complex applications.

### OOP Principles

The project makes use of the four fundamental OOP principles:

1. **Encapsulation**: 
   - The data and methods related to each object are bundled together. This improves modularity and makes the code easier to maintain.
   - Example: The `Car` class encapsulates attributes such as `model`, `year`, and methods like `start()` and `stop()`.

2. **Inheritance**: 
   - Classes can inherit properties and behavior from other classes, reducing code duplication.
   - Example: The `ElectricCar` class inherits from the `Car` class but adds its own properties such as `batteryLevel`.

3. **Polymorphism**: 
   - The ability to use a method in different ways depending on the object type. This helps in creating flexible and reusable code.
   - Example: Both `Car` and `ElectricCar` have a `drive()` method, but the implementation is different for each.

4. **Abstraction**: 
   - Hides complex implementation details and only shows the essential features of an object.
   - Example: The user interacts with a simple `drive()` method without needing to know how the internal mechanisms of the car work.

### Example Classes

```python
class Car:
    def __init__(self, model, year):
        self.model = model
        self.year = year
    
    def start(self):
        print(f'{self.model} started.')

    def stop(self):
        print(f'{self.model} stopped.')

class ElectricCar(Car):
    def __init__(self, model, year, battery_level):
        super().__init__(model, year)
        self.battery_level = battery_level

    def drive(self):
        if self.battery_level > 0:
            print(f'{self.model} is driving.')
        else:
            print(f'{self.model} cannot drive, battery is empty.')
