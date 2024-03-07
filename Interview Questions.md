Q:-Difference between Verification and Validation?
- Verification : Verification is a static process, it verify the product/feature develop is right or not and should fulfill all the requiremnets.
- Validation : Validation is dynamic process, it compare actual and expected result, checks the implementation functionality. Methods can be used Black box testing , white box testing.

Q: Can multiple Examples used in Senario Outline ?
- Yes, We can use multiple Examples

Q: How to get second last element in Xpath ?
- Position can be used

Q: Program for 
input : aabbbccccaaaaa
output :a7b3c4

**import java.util.Scanner;

   public class restAssured {
       public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Enter a string:");
        String input = scanner.nextLine();
        String compressed = compressString(input);
        System.out.println("Compressed output: " + compressed);
    }

    static String compressString(String input) {
        StringBuilder result = new StringBuilder();
        int count = 1;

        for (int i = 1; i < input.length(); i++) {
            if (input.charAt(i) == input.charAt(i - 1)) {
                count++;
            } else {
                result.append(input.charAt(i - 1));
                result.append(count);
                count = 1;
            }
        }

        // Append the last character and its count
        result.append(input.charAt(input.length() - 1));
        result.append(count);

        return result.toString();
    }
}**

  
