# Science Fair 2024
This is the code for my science fair project.

- [Descpription](#description)
    - [What does it do?](#what-does-it-do)
    - [The Algorithm](#the-algorithm)
- [Dependencies](#dependencies)
- [Build](#build)
- [Usage](#usage)
- [License](#license)



## Description
It contains two separate programs, one of which was written in C, the other written in Java. There are separate shell scripts to benchmark the time it takes for each program to run.

### What does it do?
Both programs do the same thing: calculate all prime numbers ranging from 2 to 999,958. This is done through a [prime sieve](#the-algorithm).

### The Algorithm
The algorithm used by both is called "The Sieve of Eratosthenes", and it is an algorithm that calculates primes from a given range of numbers.

It iterates through an array of numbers starting from 2 (lowest prime number), and removes its multiples (if they fit in the given range). Then, it moves onto the next number, and removes all of its numbers. This process repeats until no multiples are left, except for the primes.

The code in this repository does it slightly differently. Instead of removing from a list of numbers, it instead toggles the bits in a bitarray to 1 (at the indexes of the multiples). All of the untoggled bits are primes, and the toggled bits are multiples.



## Dependencies
Here are the packages required (debian):

- build-essential
- lld
- bc
- openjdk-17-jdk (javac)



## Build
To build the code, run `./build`.



## Usage
There are two benchmark programs for the programs:

`./bench-c` - For C program.

`./bench-java` - For Java program.



## License
This project is licensed under the [MIT](https://choosealicense.com/licenses/mit/) license.
