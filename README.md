# Method-Overriding-Super-keyword
package overiding_super;

class Animal {
    String name;
    String species;
    
    Animal(String name, String species) {
        this.name = name;
        this.species = species;
    }
    
    void makeSound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    String breed;
    
    Dog(String name, String species, String breed) {
        super(name, species);
        this.breed = breed;
    }
    
    @Override
    void makeSound() {
        super.makeSound();
        System.out.println(name + " the " + species + " of breed " + breed + " says: Woof Woof!");
    }
}

