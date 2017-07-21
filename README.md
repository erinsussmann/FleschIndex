# FleschIndex
Uses the Flesch Index to calculate the complexity of words

package fleschindex;

import java.io.FileNotFoundException;
import java.util.Scanner;

/**
 * The main method for the input of files and where the methods are called
 * @author Erin Sussmann
 * @version 4/3/17
 */
public class FleschIndex {

    public static void main(String[] args) throws FileNotFoundException {
        
        
        Scanner scan = new Scanner(System.in);
        String filename;
        String toContinue;
        
        //prompts user for a file and initilaizes it
        System.out.println("Enter a file name: ");
        filename  = scan.next();
        
        //finds document with that file name
        Document doc = new Document(filename);
        
        //prints the string of that document
        System.out.println(doc);
        
        //asks to continue with more files
        System.out.println("Do you want to process another file?");
        toContinue = scan.next();
        
       //creates loop that iterates as long as the user wants to input files
        while(toContinue.compareTo("yes") == 0)  
        {
            //prompts user for file
            System.out.println("Enter a file name: ");
            filename  = scan.next();
            
            //finds the file
            doc = new Document(filename);
        
            //prints the file
            System.out.println(doc);
        
            //asks the user to continue
            System.out.println("Do you want to process another file?");
            toContinue = scan.next();
        }  
    }   
}
