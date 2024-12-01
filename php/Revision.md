
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

## Creating a Class and an Object

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





