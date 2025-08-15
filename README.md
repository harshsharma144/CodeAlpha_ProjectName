import java.util.ArrayList;
import java.util.Collections;
import java.util.Scanner;

public class Studenttracker {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        ArrayList<Integer> grades = new ArrayList<>();
        System.out.print("Enter the number of students : ");
        int n = input.nextInt();
        input.nextLine();

        //input grades
        for (int i = 0; i < n; i++) {
            System.out.print("Enter grade for students " + (i + 1) + " : ");
            grades.add(input.nextInt());
            System.out.println("Grade added successfully!");
        }
        System.out.println("All Students Grades : " + grades);

        //Calculate Average
        double sum = 0;
        for (double grade : grades) {
            sum += grade;
        }
        double average = sum / grades.size();
      //  System.out.println("Average grade : " + average);


        //Calculate Highest and Lowest
        int highest = Collections.max(grades);
     //   System.out.println("Highest score is : " + highest);
        int lowest = Collections.min(grades);
     //   System.out.println("Lowest score is : " + lowest);

        //Summary Report
        System.out.println("\n<-- Summary Report -->");
        System.out.println("All Students Grades : " + grades);
        System.out.println("Average grade : " + average);
        System.out.println("Highest score is : " + highest);
        System.out.print("Lowest score is : " + lowest);


    }
}

