# CODESOFT
# Internship task-1
import java.util.Random;
import java.util.Scanner;
class NumberGame
{
    public static void main(String args[])
    {  
        int num,key,points=0,choice;
        char w='y';
        Scanner sc=new Scanner(System.in);
        Random random=new Random();
        do
        {
            num=1+random.nextInt(100);
            System.out.println(num);
            do
            {
                System.out.println("choose a number");
                key=sc.nextInt();
                if(key==num)
                {
                    System.out.println("your guess is correct");
                    System.out.println("you earned a point");
                    points++;
                }
                else if(key<num)
                {
                    System.out.println("your guess is small");
                }
                else
                {
                    System.out.println("your guess is high");
                }
            }while(key!=num);
            System.out.println("1.Do you play again ?");
            System.out.println("2.Do you want to know about your points");
            choice=sc.nextInt();
            System.out.println(choice);
            if(choice==1)
            {
                System.out.println("Yes or No");
                System.out.println("type Y or type N");
                w=sc.next().charAt(0);
            }
            if(choice==2)
            {
                System.out.println("your score is "+points);
            }
        }while(w=='Y');
    }
}
