# conerter
roman




import java.util.Scanner;
 
public class Main {
 
   public static void main(String[] args) {

	Scanner reader = new Scanner(System.in);
	System.out.println("Введите блять число");

	int number = reader.nextInt();
	methodOne(number);

	reader.close();
   }
 
   static void methodOne(int number) {

	String[] thousands = { "", "M", "MM", "MMM" };
	String[] hundreds = { "", "C", "CC", "CCC", "CD", "D", 
                          "DC", "DCC", "DCCC", "CM" };
	String[] tens = { "", "X", "XX", "XXX", "XL", "L", 
                          "LX", "LXX", "LXXX", "XC" };
	String[] units = { "", "I", "II", "III", "IV", "V", "VI",
                          "VII", "VIII", "IX", "X" };

	int numberOfThousands = number / 1000;

	int numberOfHundreds = (number / 100) % 10;

	int numberOfTens = (number / 10) % 10;

	int numberOfUnits = number % 10;

	String romanNumber = thousands[numberOfThousands] + hundreds[numberOfHundreds]
                             + tens[numberOfTens] + units[numberOfUnits];
	System.out.println(romanNumber);
   }
}
