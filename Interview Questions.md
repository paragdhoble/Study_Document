Q:-Difference between Verification and Validation?
- Verification : Verification is a static process, it verify the product/feature develop is right or not and should fulfill all the requiremnets.
- Validation : Validation is dynamic process, it compare actual and expected result, checks the implementation functionality. Methods can be used Black box testing , white box testing.

Q: Can multiple Examples used in Senario Outline ?
- Yes, We can use multiple Examples

Q: How to get second last element in Xpath ?
- Position can be used
  Syantx: /bookstore/book[position()>=2 and position() <= (last() - 1)]

Q: How to get Xpath for hover list?
- Ctrl shfit P >> Emulate the focus page  in inspect Element

Q: How to run Sanity or regression in Cucumber?
- @Regression @Sanity these tags can be used
- has to add in cucumber options >>tags = {"@SmokeTest"}

Q: Aggregation in SQL ?
- Having , sum ,avg , max , min used for the aggration
  
EX: TemName having multiple TeamLeads
select Teamname  , count(TeamLeads) from TeamLeads group by TeamName having count(TeamLeads) > 1

Dense_rank:
EX:
select emp , dense_rank() over ( order by salary desc) row_num from empTable where row_num = 3
select max(salary), name  from (select distinct salary, name from emptable order by salary desc fetch first 3 row only)

Q: What is WindowHand and Windowhandles and its return type?
- Return type of Windowhandles is SET

Q: Aluure report limitations?

Q:Types of Locator in selenium?
- Types of Locator
  - Id >> Id is the fastest locator as compare to others.
  - Name
  - Clas Name
  - tagsName
  - LinkText
  - partialLinkTest
  - Css Selector
  - Xpath.
 
Q: Background and Hooks , BeforeALL
-  Background is used to run common steps before all the all Scenarios within a Feature File.
-  Hooks : Hooks is a block of code that run before and after each Scenarios.We can define anywhere in the project using @Before & @After.
-  

Q: Implementation of Test runner file 
- @RunWith(Cucumber.class)
  @CucumberOptions(
   features = "Feature"
   ,glue={"stepDefinition"}
  ,tags={"@SmokeTest"}
   ,strict = true
   ,dryRun = true
)

Q: difference between driver.get and Navigate 
- get is part of WebDriver interface where navigate is part of Navigation interface.
- get doesn't have the store the history where navigate store the history and can go foward and backword.
-  driver.navigate().forward(); / driver.navigate().back();

Q: WAP to google and search the result and validate it.
- 

Q: Program to get unique words 

 Input : String str ="Welcome to Geeks for Geeks" ;
 Output :[geeks, for, to, welcome]
 
 public static void printUniqueWords (String str) {
        String[] words = str.split("\\W");
        
        HashSet < String > uniques  = new HashSet<>() ;

           for ( String  word : words) {
                    uniques.add(word.toLowerCase());
           }
           System.out.println(uniques);
    }


Q: Program to remove special character.

Input : "core$java","Selenium$framwork" , "cumcumber$testNG"
Output : [corejava, Seleniumframwork, cumcumbertestNG]


public static void removeSpecialFrmString(){

        List<String> multiWords = Arrays.asList("core$java","Selenium$framwork" , "cumcumber$testNG");

        multiWords = multiWords.stream().map(s -> s.replaceAll("\\W", "")).collect(Collectors.toList());

        System.out.println(multiWords);

}


Q: Program for 
input : aabbbccccaaaaa
output :a7b3c4

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
}

  
