import java. util. Scanner; // Importing the Scanner class in order to read what the user has to input

public class Game { // Declaring the class

public static void main (String[] args) { // This is the main method of the program and where the program starts.

int a; // Variable to store the number of times the user has tried to log in
int No_attempt = 5; //Maximum no of attempt
int guessing_Number; // Variable that holds the guess of the user

Scanner scanner = new Scanner(System. in); //_usage of the Scanner class for inputting in Java

// Remarkably, I instantiated the random number from 1 to 100.
int number = 1 + (int)(Math.random()* 100);

System. out. println("View the code Guess the number between 1 to 100");

// Loop according to the attempt
for (a = 0; a < No_attempt; a++) { // Repeated attempts are provided to the user through a ‘for’ loop
System. out. println("Guess the number:");

//Read also the guess of the user
guessing_Number = scanner. nextInt();

if(guessing_Number == number){
System. out.println("Congratulations! You guessed the number");
break;
} 

// if the user ENTERs the right guess, do not check the rest of the characters
else if (number > guessing_Number) {
System. out.println("The number is more than " + guessing_Number);
} else {
System. out. println("The number is less than " + guessing_Number);
}}

if (a == No_attempt) {
System. out.println("You have used all your tries. ");
System. out. println("The number was "+ number);
}
scanner. close(); // Closing the Scanner
}
}
