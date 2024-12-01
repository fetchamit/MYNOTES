
# OOP's In PHP
---------------
* OOP is a programming paradigm based on the concept of "objects," which can contain data (properties) and methods (functions). The primary principles of OOP are:
* Encapsulation
* Inheritance
* Polymorphism
* Abstraction

## Why Use OOP in PHP?
* It helps organize code better.
* It promotes reusability and scalability.
* It is widely used in frameworks like Laravel and Symfony.

##  Creating a Class and an Object

    <?php
    class Car {
        // Properties
        public $color;
        public $brand;
        
        // Constructor (optional)
      public function __construct($color, $brand) {
        $this->color = $color;
        $this->brand = $brand;
    }

    // Method
    public function getDetails() {
        return "This car is a {$this->color} {$this->brand}.";
      }
    }

    // Creating an object
    $myCar = new Car('Red', 'Toyota');
    echo $myCar->getDetails();
    ?>

## Access Modifiers
* Access modifiers control the visibility of class properties and methods.
1. Public: Accessible from anywhere.
2. Private: Accessible only within the class.
3. Protected: Accessible within the class and its subclasses.
* Example:

      <?php
        class Person {
        public $name;        // Accessible anywhere
        private $age;        // Accessible only in this class
        protected $salary;   // Accessible in this class and subclasses

        public function setAge($age) {
        $this->age = $age;
        }

        public function getAge() {
            return $this->age;
        }
        }

        $person = new Person();
        $person->name = "John";   // Allowed
        $person->setAge(30);      // Allowed (via public method)
        echo $person->getAge();   // Allowed
        ?>

## Inheritance
* Inheritance allows a class (child) to use the properties and methods of another class (parent).

        <?php
            class Animal {
                public $name;

                public function eat() {
                    return "{$this->name} is eating.";
                }
            }

            class Dog extends Animal {
                public function bark() {
                    return "{$this->name} is barking.";
                }
            }

            $dog = new Dog();
            $dog->name = "Buddy";
            echo $dog->eat();   // Output: Buddy is eating.
            echo $dog->bark();  // Output: Buddy is barking.
        ?>









