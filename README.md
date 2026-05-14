\*prime_number_checker_c-language
This is just a simple program for C language to check prime no...*\

  #include <stdio.h>

    int main() {
        int n; // Variable to store the number to check for primality
        int prime=0; // Flag to indicate if n is prime (0 means prime, 1 means not prime)

        printf("Enter a number to check if it is prime: ");
        scanf("%d", &n); // Read the number from user input
        if(n<=1){
            printf("%d is not a prime number\n", n); // 0 and 1 are not prime numbers
            return 0;
        }

        for(int i=2; i<n; i++){
            if(n%i==0){
                prime=1;
                break; // If n is divisible by any number between 2 and n-1, it is not prime
            }
        }

        if(prime==0){
            printf("%d is a prime number\n", n);/* This prints that the number is prime */
        }
        else{
            printf("%d is not a prime number\n", n); // This prints that the number is not prime
        }

        return 0;
    }
