import java.time.LocalDate;
import java.util.Locale;
import java.util.Scanner;
public class lab2E2 {
    public static void main(String[] args) {
        Scanner console=new Scanner(System.in).useLocale(Locale.US);

        System.out.println("Enter your age");
        int age=console.nextInt();
        System.out.println("your age is: "+age);

        System.out.println("Enter your weight");
        double weight=console.nextDouble();
        System.out.println("your weight is: "+weight);

        System.out.println("Enter your Heart best per Minutes");
        int Heart=console.nextInt();
        System.out.println("your Heart best per Mintues is: "+Heart);

        System.out.println("Enter the amount of exercising time");
        int time=console.nextInt();
        System.out.println("your age is: "+time);

        System.out.println("Calories"+calculateCalories(age,weight,Heart,time)+" calories");
        System.out.println("Report Date: "+ LocalDate.now());
    }
    public static double calculateCalories(int age,double weight,int Heart,int time ){
        return ( ( (age * 0.2757) + (weight * 0.03295) + (Heart  * 1.0781) - 75.4991 ) * time / 8.368);

    }
}
