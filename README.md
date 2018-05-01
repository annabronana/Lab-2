# Lab-2
String Manipulator Lab

Almost Complete version, only thing left is to finish Replace Single.

import java.util.Scanner;

public class StringManipulator {
public static void main(String[] args) {
	
	boolean bool = true;
	
	while (bool == true) {	
		//Creates a scanner for user input and asks
		//for user to input a phrase.
		Scanner scanner = new Scanner(System.in);
		System.out.print('\n' + "Please enter a phrase: ");
		String userInput = scanner.nextLine();
		if (userInput.length() == 0) {
			bool = false;
		}
		String emptyString = ("");
		//Prints the manipulation options for the 
		//user to choose from.
		System.out.println("1. Print Reverse");
		System.out.println("2. Replace");
		System.out.println("3. Remove");
		System.out.println("4. Quit" + '\n');
		//to choose which manipulator option they want to use.
		System.out.print("Please choose an option: ");
		String optionChoice = scanner.nextLine();
		optionChoice = optionChoice.toLowerCase();
		//Conditional that runs a for loop if they input
		//'print reverse' capitalized or not capitalized.
		if (optionChoice.equals ("print reverse")){
			//The for loop starts and iterates from the end of
			//the phrase and concatenates each letter together backwards.
			for (int  i= userInput.length()-1; i >= 0; i -- ) {
				char eachChar = userInput.charAt(i);
				String backPhrase = emptyString + eachChar ;
			System.out.print(backPhrase);
		}
		}
		if (optionChoice.equals ("replace")){
			System.out.print("What character would you like to replace? ");
			String oldCharInput = scanner.nextLine();
			if ((oldCharInput.length() == 0) || (oldCharInput.length() >1)){
				
			}
			else {
			char oldChar = oldCharInput.charAt(0);
			System.out.print("What character would you like to replace it with? ");
			String newCharInput = scanner.nextLine();
			if (userInput.contains(oldCharInput)){
				if ((newCharInput.length() == 0) || newCharInput.length() > 1) {
					
				}
				else {
				char newChar = newCharInput.charAt(0);
				for (int i=0; i< userInput.length(); i++) {
				
					if (userInput.charAt(i)==oldChar) {
						System.out.print(newChar);
					}
				else {
					System.out.print(userInput.charAt(i));
				}
			}
			
				

				}
			}
			else {
				System.out.print("That character is not in your phrase.");
			}
		}
		}
		
		
				
		if (optionChoice.equals ("replace single")) {
			System.out.print("What character would you like to replace? ");
			String oldCharInput = scanner.nextLine();
			if ((oldCharInput.length() == 0) || (oldCharInput.length() >1)){
				
			}
			else {
			char oldChar = oldCharInput.charAt(0);
			System.out.print("What character would you like to replace it with? ");
			String newCharInput = scanner.nextLine();
			if (newCharInput.length() == 0  || (newCharInput.length() >1)){
			
			}
			else {
			char newChar = newCharInput.charAt(0);	
			System.out.print("Which "  + oldChar +  " would you like to replace? ");
			String charInst = scanner.nextLine();
			char charInstChar = charInst.charAt(0);
			if (Character.isDigit(charInstChar)) {
			int charInstInt = Integer.parseInt(charInst);
			int charInstNum = (charInstInt);
			int count = 0;
			if (userInput.contains(oldCharInput)) {
				if ((newCharInput.length() == 0) || newCharInput.length() > 1) {
				}
				else {
				for(int i=0; i<userInput.length(); i++) {
					if (userInput.charAt(i)==oldChar) {
						count ++;
						if (count == charInstNum) {
							System.out.print(newChar);
						}
						else {
							System.out.print(userInput.charAt(i));
							}
					
					}
					else {
						System.out.print(userInput.charAt(i));
					}
					
					}
				}
			}
			else {
				System.out.print("That character is not in your phrase.");
				
			}
			
			}
		}
		}
		}
	
		if (optionChoice.equals("remove")) {
			System.out.print("What character would you like to remove? ");
			String oldCharInput2 = scanner.nextLine();
			if (userInput.contains(oldCharInput2)) {
				if ((oldCharInput2.length() == 0) || oldCharInput2.length() > 1) {
					
				}
				else {
					char oldChar2 = oldCharInput2.charAt(0);
					for (int i = 0; i< userInput.length(); i ++) {
						if (userInput.charAt(i)==oldChar2) {
							System.out.print("");
					}
						else {
							System.out.print(userInput.charAt(i));
					
					}
					}
	
			}
			}
			else {
				System.out.print("That character is not in your phrase.");
		}
		}
		
		if (optionChoice.equals("quit")) {
			bool = false;
			System.out.print("Quitting...");
			System.exit(0);					
		}
		}
		}
		}
