## TestNG Questions
1.What are the annotations used in TestNG?
There are three sections of Annotaions Testing
a.Precondition annotation 
The TestNG annotation which are run before TestNG
@BeforeSuite , @BeforeTest, @BeforeClass, @BeforeMethod

b.Test Annotation
This is the annotation which is only mentioned before the test case (Before the method written to execute the test case)
@Test

c.Postcondition annotations
These are the annotations that are executed after the test case. (After the method is written to execute the test case)
@AfterSuite, @AfterClass, @AfterTest, @AfterMethod 


2.What is the sequence of execution of the annotations in TestNG?
@BeforeSuite
@BeforeTest
@BeforeClass
@BeforeMethod
@Test
@AfterMethod
@AfterClass
@Aftertest
@AfterSuite

3.How to set priorities in TestNG?
This is used to set the priorities of the Test Cases if the priorities not set then it will execute alphabetically
If we want to give a test method, priority higher than the default priority then we can simply assign a negative value to the priority attribute of that test method.
Test with no priorities will execute first and have the default value 0
EX:-
@Test (priority=1), @Test (priority=2)

4.How will you define grouping in TestNG?
We can used group attribute for grouping
EX:-
@Test(groups ="title")

5.What is a dependency on TestNG?
There are some method on which othere methods are dependent on 
EX:-
@Test(dependsOnMethods="LoginTest")


6.What is InvocationCount in TestNG?
If need to execute a Test multiple time we used invocationCount 
EX:-
@Test (invocationCount = 8)

7.What is timeOut in TestNG?
If some test is taking time to execute we can used timeOut to terminate that and will fail the Test case
@Test(timeOut =5000) it will be in millisec


8.How to handle exceptions in TestNG?
There are some expected exceptions while running the Test we can define explicilty in Test annotation so that Test Cases will not fail
@Test(expectedException=numberFormatException.class)

9.What are the common TestNG assertions?
Assert.assertEquals(String actual ,String expected)
Assert.assertTrue , Assert.assertFalse


10. How to disable a test in TestNG?
To disable the Test cases we can use this
@Test (enable = "false" )

11.What are the types of Asserts in TestNG?
There are two type of assert 
a. Hard Assert: Test ccases will fail and stop the execution if the condtiin will fail
Assert.assertEquals(actual , expected)

b.Soft Assert : Test case will keep on running if the assertion get fail
we have to create the object of soft assert
softAssert assert = new softAssert();
assert.assertAll();

12.How to pass parameter in the test case through the testng.xml file?
We can pass the parameter in the Test case through parameter and can define in TestNG.xml

@Parameter("username", "password")
@Test
public logIn()
{
driverget(“appname”);
driver.findElement(By.id(“login”)).sendkeys(username);
driver.findElement(By.id(“password”)).sendkeys(password);
}

XML File
<Suite name = “suitename”>
<test name =”testname”>
<parameter name =”username” value=”user1”/>
<parameter password =”password” value =”pass1”/>
<Classes>
<class name =”passingparameters”/>
<classes/>
<test/>
<Suite/>

13.What is the return type of @DataProvider annotation provided by TestNG?
@DataProvider annotation return an object double array (Object[ ][ ]) as data to the test method.


14.Which attribute is used to run test method always?
to run the Test Case always we can use
@Test(alwaysRun = True)












