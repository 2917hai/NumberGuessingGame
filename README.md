# NumberGuessingGame
# I have made NumberGuessingGame between 1 to 100 with help of java
import java.util.Random;
import java.util.Scanner;
public class NumberGuessingGame
{
    public static void main (String []args)
    {
        int userGuess=0;
        int computerGuess;
        int attempts=0;
        boolean hasGuessingEqual= false;
        Scanner sc= new Scanner(System.in);
        Random rd = new Random();
        computerGuess= rd.nextInt(1,100);

        System.out.println("hii wellcom to the Number Guessing Game");
        System.out.println("I have selected a number between 1 to 1oo   So friends Guess the number");

        while (!hasGuessingEqual)
        {
            try
            {
                System.out.println(" So guess a number");
                userGuess= sc.nextInt();
            }
            catch (NumberFormatException e)
            {
                System.out.println(" please enter a valid number");
            }
            attempts++;
            if(userGuess < computerGuess)
            {
                System.out.println("your guess number is low");
            }
            else if (userGuess > computerGuess)
            {
                System.out.println(" your guess number is high ");
            }
            else
            {
                hasGuessingEqual=true;
                System.out.println("congratulation you have guessed the number "+computerGuess +" in "+attempts+" attempts");
            }
        }
    }
}
