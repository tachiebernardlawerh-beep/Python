const readlineSync = require('readline-sync');

// Function to check if a number is prime
function isPrime(num) {
    // Numbers less than 2 are NOT prime
    if (num < 2) {
        return false;
    }

    // Check for factors from 2 up to the square root of the number
    for (let i = 2; i <= Math.sqrt(num); i++) {
        if (num % i === 0) {
            return false; // Found a factor, so it's not prime
        }
    }

    return true; // No factors found, it is prime
}

// Main function to run the program
function main() {
    // Use readlineSync.questionInt() to read an integer from the user
    const userInput = readlineSync.questionInt('Enter an integer to check if it is prime: ');

    // Call isPrime() and print the result
    if (isPrime(userInput)) {
        console.log(`${userInput} is a prime number.`);
    } else {
        console.log(`${userInput} is NOT a prime number.`);
    }
}

// Execute the main function
main();
# Python