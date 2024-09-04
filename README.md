URL to demonstration video https://youtu.be/YE5vOR2VXhQ?si=G4kD8SXq0guB-71k

Inheritance 

The class hierarchy in the program is structured with a base class, 'Pokemon,' which is inherited by specialized subclasses such as 'ElectricPokemon,' 'FirePokemon,' and 'WaterPokemon.' These subclasses inherit both properties and methods from the 'Pokémon' class. Subclasses, like Water Pokémon, use extends to inherit and enhance features from the parent Pokémon class. The super keyword in subclass constructors ensures proper initialization by explicitly invoking the superclass constructor. Notably, they override the 'attack' method and use the "instance of" comparison to determine the target class. 

This inheritance model serves to encapsulate shared attributes and methods common to all Pokemon in the 'Pokemon' base class. It allows specific Pokemon types to inherit, override, or extend functionalities as required. By reusing common characteristics across all Pokemon and tailoring attack behavior to each specific type, the design promotes code reusability and maintains a clear and organized class hierarchy.  

 

Polymorphism 

The base class 'Pokemon' declares a polymorphic method named 'attack,' which is overridden by each of its subclasses. Additionally, the 'Battle' class interacts with 'Pokemon' objects without requiring knowledge of their specific types. It simplifies the code and allows for a more adaptable and extensible design. 

 
Abstraction 

Abstraction is manifested in the design of the Pokemon class, which serves as an abstract base class encapsulating common attributes like name, type, and grade. By declaring an abstract method (attack), it abstracts away the specifics of how each Pokémon attacks. This design promotes modularity and extensibility, making the system more understandable and maintainable. 

 

Encapsulation 

In our code, encapsulation is implemented by declaring class fields as private, restricting direct access to these fields from outside the class. For example, we set the attributes like name, type, grade, and others in the Pokemon class are private, ensuring that their values can only be accessed or modified through getter and setter methods. These methods, in turn, provide controlled access to the encapsulated data. Similarly, in the Player class, private instance variables like name, player_pokemons, and score are accessed and manipulated through public methods like addPokemon, pokemondead and addScore. This encapsulation of internal details within classes promotes modularity and information hiding, contributing to a more organized and secure codebase. 

 


Static Class 

The static class Art in the provided Java code serves a specific purpose by encapsulating all method that responsible for rendering an ASCII art representation of different Pokémon. This class follows the concept of encapsulation, bundling the drawing logic within a dedicated class, promoting code organization and modularity. The method's static nature indicates that it can be invoked without creating an instance of the Art class, providing a convenient and efficient way to draw the Pokémon's ASCII art. The ASCII art itself is a creative and visually descriptive representation of Pokémon, enhancing the aesthetic appeal of the program output. 

 

 

 

2.2 Add-on Features 

 
Add-on Features 1: ASCII Art 
The integration of ASCII art into our Java program aimed to add a visually appealing element to the user interface. ASCII art not only serves an aesthetic purpose but also contributes to a more engaging and enjoyable user experience.We employed a modular approach to implement ASCII art, creating a separate class responsible for generating and displaying ASCII art. The integration process involved the following key steps: 

Create a java static class file called “Art” 

Create ASCII art of all pokemons in the database 

Create methods to draw pokemon (e.g. public static void drawEntei()) which prints ASCII art of specified pokemons and store them in the “Art” file. 

Call the methods when enemy pokemon or player pokemon appears 

We Integrated the ASCII art module seamlessly into the user interface, ensuring it complements the existing design and does not disrupt the overall user experience. These methods are crafted with reusability and ease of adding more arts in mind. 

 

 
Add-on Features 2: Ga-Olé Disk 
The addition of the "convertDisk()" method allows the player to get Ga Olé Disk of defeated and caught Pokémon. This method is made to enhance user experience by making it as similar to the arcade game as possible and foster a sense of achievement. Here are the key steps: 

Create a convertDisk() method in the same file 

Call the method when after completing the game 

Print player Pokémon list to convert to Ga Olé Disk 

Ask user if they want to convert them to Ga Olé Disk and receive their input 

Print response line depending on user input. 

This is a simple method, but it complements the design of the Game. This makes the game feel whole and complete with its closing prompt and gratitude for playing. 

 

 

 

Add-on Features 3: Critical Hit Rate 
A critical hit rate feature is also added among others. During player or enemy attacks, the attack power won't remain constant. Here is how it works: 

Set MIN_VALUE and MAX_VALUE to 0.3 and 0.99 respectively 

Create ThreadLocalRandom.current().nextDouble(MIN_VALUE, MAX_VALUE) method to use the random decimal. 

Use method in battle.java for playerTurn() and enemyTurn() to calculate total damage that will be dealt. 

The methods are called when either side Pokémon's attack each other during the game 

It dynamically adjusts from the base attack value, modified by comparing it with the attributes of the enemy Pokémon, and is then divided by a random decimal between 0.3 and 0.99 to form a critical hit rate. This adds an element of unpredictability, making the entire game more thrilling and filled with unknown variables. 

 

 

 

 

 


