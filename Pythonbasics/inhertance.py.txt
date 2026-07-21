class Animal:
    def speak(self):
        print("sound")

class Dog(Animal):
    def speak(self):
        print("Dog")

pet = Dog()
pet.speak()