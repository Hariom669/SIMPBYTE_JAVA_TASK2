# SIMPBYTE_JAVA_TASK2

import java.util.Scanner;
public class examinaton {




        public static void main(String[] args) {

            Scanner input = new Scanner(System.in);

            // User Login
            System.out.print("Enter Username: ");
            String username = input.nextLine();

            System.out.print("Enter Password: ");
            String password = input.nextLine();

            // Profile Update
            System.out.print("Would you like to update your profile? (Y/N): ");
            String updateProfile = input.nextLine();

            if (updateProfile.equalsIgnoreCase("Y")) {
                System.out.print("Enter New Username: ");
                username = input.nextLine();

                System.out.print("Enter New Password: ");
                password = input.nextLine();
            }

            // MCQs
            System.out.println("Please answer the following questions: ");
            System.out.println("1. What is the capital of France?");
            System.out.println("A. Paris\tB. London\nC. Rome\tD. Berlin");
            String answer1 = input.nextLine();

            System.out.println("2. What is the highest mountain in the world?");
            System.out.println("A. Mount Everest\tB. K2\nC. Kangchenjunga\tD. Lhotse");
            String answer2 = input.nextLine();

            // Timer and Auto-submit
            int timer = 60; // in seconds
            while (timer > 0) {
                System.out.println("Time Remaining: " + timer + " seconds");
                try {
                    Thread.sleep(1000); // delay for 1 second
                    timer--;
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
            }

            // Closing Session and Logout
            System.out.println("Time's up! Your answers have been automatically submitted.");
            System.out.println("Thank you for taking the exam!");
        }
    }


