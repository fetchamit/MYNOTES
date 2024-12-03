
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

## Polymorphism
* Polymorphism allows methods to have different implementations in different classes.

        <?php
            class Shape {
                public function calculateArea() {
                    return "Area calculation depends on the shape.";
                }
            }

            class Circle extends Shape {
                public function calculateArea($radius) {
                return pi() * $radius * $radius;
                }
            }

            class Rectangle extends Shape {
                public function calculateArea($length, $width) {
                    return $length * $width;
                }
            }

        $circle = new Circle();
        echo $circle->calculateArea(5); // Circle area

        $rectangle = new Rectangle();
        echo $rectangle->calculateArea(10, 5); // Rectangle area
        ?>

  Note: Method Overloading is not supported in PHP.

## Abstract Classes and Interfaces
* Abstract Class: Can have both defined and undefined (abstract) methods.
* Interface: All methods must be implemented by the class that uses it. An Interface can not contain a data members.
* Example of Abstract class:

      <?php
            abstract class Vehicle {
                abstract public function move();

                public function fuel() {
                    return "Fueling...";
                }
            }

          class Bike extends Vehicle {
                public function move() {
                    return "Bike is moving.";
                }
        }

        $bike = new Bike();
        echo $bike->move();  // Output: Bike is moving.
        echo $bike->fuel();  // Output: Fueling...
        ?>

* Example of Interface

        <?php
            interface Logger {
                public function log($message);
            }

            class FileLogger implements Logger {
                public function log($message) {
                    echo "Logging to a file: $message";
                }
            }

            $logger = new FileLogger();
            $logger->log("Hello World!");
        ?>

## Traits
* Traits is a special function, Traits allow you to reuse code in multiple classes.
* Example

      <?php
            trait Logger {
                public function log($message) {
                    echo "Logging: $message";
                  }
              }

            class User {
                use Logger;
            }

            class Product {
                use Logger;
            }

            $user = new User();
            $user->log("User created.");

            $product = new Product();
            $product->log("Product added.");
        ?>

  ## Namespaces
  * Namespaces are the collection of multiple classes.
  * Namespaces in PHP are used to organize code into logical groups and avoid name conflicts in larger applications. This is especially useful when integrating third-party libraries.
  * Example

        <?php
            namespace App\Models;

            class User {
                public function getName() {
                    return "John Doe";
                }
            }

            namespace App\Controllers;

            use App\Models\User;

            $user = new User();
            echo $user->getName();
        ?>

## Magic Methods
1. __get()
* Triggered when trying to access an undefined or private property.

        class Test {
            private $data = [];

              public function __get($name) {
                return $this->data[$name] ?? null;
                }
            }

            $obj = new Test();
            echo $obj->nonexistentProperty; // Output: null

2. __set()
* Triggered when trying to set an undefined or private property.

          class Test {
               private $data = [];

                public function __set($name, $value) {
                    $this->data[$name] = $value;
                }
            }

            $obj = new Test();
            $obj->name = "PHP";
3. __call() - For inaccessible methods
4. __toString() - For string representation











