# GPA-Calculator
this program will calculate your gpa and cgpa
im a CS student currently studying in University.
<-- program starts here -->
import java.util.Scanner; 
  
public class GPA {
  
  public static void main(String[] arges){
    Scanner input = new Scanner(System.in);
  
    int incourses;
    float ch = 0;
    float[] array = new float[10];
    float[] array2 = new float[10];
    float[] array3 = new float[10];
    float sumofgrade = 0;
    float sumofch = 0;
    
    System.out.println("How many course have you taken in your current semester?");
    incourses = input.nextInt(); /** takes input of how many courses from user */
    
    System.out.println("Enter credit hour for each course");
    
    for(int a = 0; a < incourses; a++)
    {
      System.out.print("course" + " " + (a+1) + " " + "credit hours = " );
      ch = input.nextInt();
      array[a] = ch; /** array to take in credit hours from user */
    }
    System.out.print("Enter the obtained grades of each course: ");
    for(int b = 0; b < incourses; b++)
    {
      System.out.println("course" +" " + (b+1)+ " " + "Grades obtained =" );
      ch = input.nextFloat();
      array2[b] = ch;/** array to take in obtained gardes of each respective course from user */
    }
     
     
    for(int c = 0; c < incourses; c++){
      
      array3[c] = (array[c] * array2[c]); /** multiply each courses' credit hours with obtained grades respectively */
     
    }

    for(int d = 0; d < incourses; d++)
    {
      sumofgrade += array3[d]; /** add the result of multiplication of credit hours and obtained grades */
      sumofch += array[d]; /** add all the credit hours */
    }
    float gpa = sumofgrade / sumofch; 
    
    System.out.println("Your GPA = " + gpa);
  }
  
}
CGPA CALUATOR CODE-------


package gpa;

import java.util.Scanner;
public class Cgpa {
    
public void display()
{
     Scanner input = new Scanner(System.in);
     int sem;
     int[] array = new int[10];
     float[] array2 = new float[10];
     int sumOfCh = 0;
     float total = 0;
     
     System.out.println("What semester are u currently in?");
     sem = input.nextInt();
     
     for(int a=0; a<sem; a++){
         System.out.println("Enter semester no."+" "+ (a+1)+ "credit hour.");
         array[a] = input.nextInt();
     }
     
     for(int b=0; b<sem; b++){
         System.out.println("Enter ur gpa of semester no."+" "+ (b+1));
         array2[b] = input.nextFloat();
     }
     for(int c=0; c<sem; c++){
         
         sumOfCh += array[c];
         total += array[c] * array2[c];
         
     }
     System.out.println(total);
     
    float cgpa = 0;
    cgpa = total / sumOfCh;
    System.out.println("Cgpa = "+ cgpa);
}

}
