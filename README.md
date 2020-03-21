# practice
def greeting(name):
  print "Hello, " + name
  
def password_req(password):
  if len(password) <= 8 or len(password) >= 17:
    return "Passwords must be between 8 and 17 characters."
  return "Password updated successfully."

# practice creating classes, methods, and functions
class Clothing:
  stock = {'name': [], 'material': [], 'amount': []}
  def __init__(self, name)
    material = ""
    self.name = name
  def add_item(self, name, material, amount):
    Clothing.stock['name'].append(self.name)
    Clothing.stock['material'].append(self.material)
    Clothing.stock['amount'].append(amount)
  def Stock_by_Material(self, material):
    count = 0
    n = 0
    for item in Clothing.stock['material']:
      if item == material:
        count += Clothing.stock['amount'][n]
        n += 1
    return count
    
class shirt(Clothing):
  material = "Cotton"
class pants(Clothing):
  material = "Cotton"
  
polo = shirt("Polo")
sweatpants = pants("Sweatpants")
polo.add_item(polo.name, polo.material, 4)
sweatpants.add_item(sweatpants.name, sweatpants.material, 6)
current_stock = polo.Stock_by_Material("Cotton")
print(current stock)

# practice with code reuse
class Animal:
  name = ""
  category = ""
  
  def __init__(self, name):
    self.name = name
  
  def set_category(self, category):
    self.category = category

class Turtle(Animal):
  name = "turtle"
  category = "reptile"
  
class Snake(Animal):
  name = "snake"
  category = "reptile"
 
class Zoo:
  def __init__(self):
    self.current_animals = {}
  
  def add_animals(self, animal):
    self.current_animals[animal.name] = animal.category
  
  def total_of_category(self, category):
    result = 0
    for animal in self.current_animals.values():
      if animal == category:
        result += 1
    return result

zoo = Zoo()

turtle = Turtle("Turtle") #create an instance of the Turtle class
snake = Snake("Snake") #create an instance of the Snake class

zoo.add_animal(turtle)
zoo.add_animal(snake)

print(zoo.total_of_category("reptile")) #how many zoo animal types in the reptile category
