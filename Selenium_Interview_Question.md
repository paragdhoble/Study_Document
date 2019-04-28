# Study_Document

1.	Version of selenium jar, testng jar, geckoDriver.exe, IEDriverServer.exe, chromeDriver.exe and All browsers version
2.	Why Selenium
3.	How does the selenium WebDriver work?
4.	Selenium WebDriver Architecture
5.	Different types of WebDrivers
6.	Open browser in specific dimension
7.	Webdriver methods
8.	Locator types
9.	Types of assertion
10.	difference between assert and verify commands
11.	Difference between HardAssert and SoftAssert
12.	Types of wait
13.	Frames and Windows navigation
14.	Alertand pop up handling
15.	Mouse over
Questions related to TestNG
16.	Junit and testNG
17.	Benefits of TestNG over Junit
18.	Parameterization in TestNG
19.	Listeners in testng
20.	Run testing.xml from cmd
21.	Run testcase for multiple times in testing
22.	Detect test failure in testng @AfterMethod
23.	Test priority in testng
24.	Exception in test
25.	How to run testcases parallel in testng


26.	Exceptions in Selenium Webdriver
27.	Difference between xpath and cssselector
28.	What is absolute and relative xpath
29.	Xpath and cssselector examples. Find element by cssSelector
30.	Difference between driver.close() and driver.quite()
31.	Double click
32.	Selenium grid
33.	How to take screenshot in selenium
34.	Database connectivity
35.	Read data from property file
36.	Read data from XML file
37.	Read/Write data from excel file
38.	Select class (dropdown)
39.	Scrolling in Selenium
40.	Framework types
41.	Desired Capabilities? How to open firefox, chrome and IE on remote machine
42.	How to open firefox, chrome and IE on remote machine
43.	Ways to refresh the browser
44.	Handling Dynamic web tables using selenium webdriver





1.	Version of selenium jar, Testngjar, geckoDriver.exe, IEDriverServer.exe, ChromeDriver.exe and all browser
1.	Selenium - selenium-server-standalone-3.8.1.jar
2.	Testng - testng-6.8.5.jar
3.	GeckoDriver - 0.19.1
4.	IEDriverServer - 
5.	ChromeDriver- 2.37
6.	FireFox - 57.0.3
7.	IE - 11.0.43
8.	Chrome - 64.0.3282.186


2.	Advantages and Disadvantages of selenium
I) Advantages of Selenium
1) Selenium is an Open Source Software.
2) Selenium supports various programming languages to write programs (Test scripts)	(Java, C#, Perl, Python, Ruby and PHP)
3) Selenium supports various operating systems (MS Windows, Linux, Macintosh etc...)
4) Selenium supports various Browsers (Mozilla Firefox, Google Chrome, IE, Opera, Safari etc...)
5) Selenium supports Parallel Test Execution.
6) Selenium uses less Hardware resources.

II) Disadvantages of Selenium
1) It supports Web based applications only.
2) No Built-in Reporting facility.
3) Difficult to Setup Test Environment when it compares to Vendor Tools like UFT, RFT, SilkTest etc..
4) No reliable Technical Support from anybody.	


3.	How does the selenium webDriver work?
When the automation script is executed, the following steps happen:
1. for each Selenium command, a HTTP request is created and sent to the browser driver 
2. the browser driver uses a HTTP server for getting the HTTP requests
3. the HTTP server determines the steps needed for implementing the Selenium command 
4. the implementation steps are executed on the browser 
5. the execution status is sent back to the HTTP server
6. the HTTP server sends the status back to the automation script



4.	Selenium WebDriver Architecture

 

There are four components of Selenium Architecture:
1. Selenium Client Library
2. JSON Wire Protocol over HTTP
3. Browser Drivers
4. Browsers

1. Selenium Client Libraries/Language Bindings:
Selenium supports multiple libraries such as Java, Ruby, Python, etc., Selenium Developers have developed language bindings to allow Selenium to support multiple languages.

2. JSON WIRE PROTOCOL over HTTP Client:
JSON stands for JavaScript Object Notation. It is used to transfer data between a server and a client on the web. JSON Wire Protocol is a REST API that transfers the information between HTTP server. Each BrowserDriver (such as FirefoxDriver, ChromeDriver etc.,) has its own HTTP server.

3. Browser Drivers:
Each browser contains separate browser driver. Browser drivers communicate with respective browser without revealing the internal logic of browser’s functionality. When a browser driver is received any command then that command will be executed on the respective browser and the response will go back in the form of HTTP response.

4. Browsers:
Selenium supports multiple browsers such as Firefox, Chrome, IE, Safari etc.


5.	Different types of webdrivers
The different drivers available in WebDriver are:
1.	FirefoxDriver
2.	InternetExplorerDriver
3.	ChromeDriver
4.	SafariDriver
5.	OperaDriver
6.	AndroidDriver
7.	IPhoneDriver
8.	HtmlUnitDriver
9.	GeckoDriver

6.	Open browser with specific dimension
Dimension d = new Dimension(800,480);  // width=800, height=480
//Resize current window to the set dimension
driver.manage().window().setSize(d);


7.	WebDriver methods
A)	Browser methods
i)	get()   ex:- driver.get(URL);
ii)	getTitle()
iii)	getPageSource()
iv)	getCurrentUrl()
v)	getWindowHandle()
vi)	close()
vii)	quit()
B)	Browser navigation methods
i)	navigate().to();
ii)	navigate().refresh();
iii)	navigate().back();
iv)	navigate().forword()
C)	methods on webElement
i)	sendKeys()
ii)	click();
iii)	clear();
iv)	isEnabled()
v)	isDisplayed()
vi)	isSelected()
vii)	getText()
viii)	getAttribute()
D)	other
i)	manage().window().maximize()
ii)	manage().window().setSize(dimensionObject)


8.	Locator types
The locator can be termed as an address that identifies a web element uniquely within the webpage.
	1) ID
	2) ClassName
	3) Name
	4) TagName
	5) LinkText
	6) PartialLinkText
	7) Xpath
	8) CSS Selector


9.	Types of assertion
10.	Difference between Assert and Verify Command

Assertions verify that the state of the application is same to what we are expecting.
Assertions in selenium can be used in 3 modes which are explained below:
1. Assert:test gets aborted if the assert fails.
	Example:- 
	assertTrue(driver.getPageSource().contains("Selenium));
	
2. Verify: test case will not abort even if the verify fails.
	Example:-
	if(driver.getPageSource().contains("Selenium"))
	{
		System.out.println("Text is Present");
	}
	
3. waitFor:waitFor command waits for the condition to become true. If the condition is true already the test case continues else it waits for the conditions to become true. If the condition doesn’t becomes true within specified time-out period test will fail and halt.


11.	Difference between HardAssert and SoftAssert
HardAssert: - A hard assert throw AssertException immediately after a test fails and the test is marked as failed.
	1) Assert.assertEquals(actual,expected); 2) Assert.assertNotEquals(actual,expected);
	3) Assert.assertTrue(condition);	4) Assert.assertFalse(condition);
	5) Assert.assertNull(object);	6) Assert.assertNotNull(object);
SoftAssert: - Soft Assert collects errors during @Test. Soft Assert does not throw an exception when an assert fails and would continue with the next step after the assert statement.
	SoftAssertSoftAssertObject= new SoftAssert();
	SoftAssertObject.assertEquals("test", "test");
	SoftAssertObject.assertTrue(false);
	SoftAssertObject.assertAll();


12.	Types of wait
There is 2 different way to handle this using waits:
  1. Implicit Waits
  2. Explicit Waits

1. Implicit Waits
		WebDriver waits for an element if they are not immediately available. So, WebDriver does not throw NoSuchElementException immediately. This is known as implicitlyWait(). This can be achieved using:
	driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);

Disadvantages:
(i) In any case, it blindly wait for given seconds.
(ii) Once set, the implicit wait is set for the life of the WebDriver object instance.

2. Explicit Waits
A. Thread.sleep()
This is to wait the running program for some time, this can be done using:
Thread.sleep(3600).
Disadvantages:
(i) In this case, it again blindly wait for given seconds.
(ii) Some computers are slow, an element may not show up in a slow computer within the given wait time.

B. Expected Condition
		An explicit wait is code you define to wait for a certain condition to occur before proceeding further in the code. There are some convenient methods provided that help you to write code that will wait only as long as required. WebDriverWait in combination with ExpectedCondition is one way this can be accomplished.

Ex.-WebDriverWait wait = new WebDriverWait(driver, 15);
WebElement element = wait.until(ExpectedConditions.presenceOfElementLocated(By.id()));

This waits up to 15 seconds before throwing a TimeoutException or if it finds the element will return it in 0 – 15 seconds. WebDriverWait by default calls the ExpectedCondition every 500 milliseconds until it returns successfully. A successful return is for ExpectedCondition type is Boolean return true or not null return value for all other ExpectedCondition types.

Ex.-WebDriverWait wait = new WebDriverWait(driver, 15);
WebElement element = wait.until(ExpectedConditions.elementToBeClickable(By.id()));

3.Fluent Wait Command: Each FluentWait instance defines the maximum amount of time to wait for a condition, as well as the frequency with which to check the condition. Furthermore, the user may configure the wait to ignore specific types of exceptions while waiting, such as ‘NoSuchElementExceptions’ when searching for an element on the page.
	Ex.- 1)  Wait wait = new FluentWait(driver)
			.withTimeout(30, SECONDS)
			.pollingEvery(5, SECONDS)
			.ignoring(NoSuchElementException.class);
			wait.until(ExpectedConditions.elementToBeClickable(By.id()));
Ex:- 2)
WebDriver driver = new FirefoxDriver();
		driver.get("http://toolsqa.wpengine.com/automation-practice-switch-windows/");
FluentWait<WebDriver> wait = new FluentWait<WebDriver>(driver);
		wait.pollingEvery(250,  TimeUnit.MILLISECONDS);
		wait.withTimeout(2, TimeUnit.MINUTES);
		wait.ignoring(NoSuchElementException.class); //make sure that this exception is ignored
Function<WebDriver, WebElement> function = new Function<WebDriver, WebElement>()
			{
				publicWebElement apply(WebDriver arg0) {
					System.out.println("Checking for the element!!");
					WebElement element = arg0.findElement(By.id("target"));
					if(element != null)
					{
						System.out.println("Target element found");
					}
						return element;
					}
				};
				wait.until(function);
			}
	
Possible ExpectedConditions:-
	elementToBeClickable, alertIsPresent(), elementToBeSelected, frameToBeAvailableAndSwitchToIt, presenceOfElementLocated

13.	Frames and Window navigation
Switching between frames:-
We can switch frames using 2 ways.
	1) By Index
		driver.switchTo().frame(0);
	2) By Name or Id
		driver.switchTo().frame("iframe1");
		driver.switchTo().frame("id of the element");

	To move back to the parent frame, you can either use switchTo().parentFrame() or if you want to get back to the main (or most parent) frame, you can use switchTo().defaultContent();
	driver.switchTo().parentFrame();
	driver.switchTo().defaultContent();


Switching between windows:-
String parentWindow = driver.getWindowHandle();
Set<String> windows=driver.getWindowHandles();
		
	for(String s1 : windows) {
		if(s1!=parentWindow) {
			driver.switchTo().window(s1);
		}
	}


14.	Alert and pop up handling
WebDriver offers the users with a very efficient way to handle these pop-ups using Alert interface. There are the four methods that we would be using along with the Alert interface.

void dismiss() – The dismiss() method clicks on the “Cancel” button as soon as the pop-up window appears.
void accept() – The accept() method clicks on the “Ok” button as soon as the pop-up window appears.
String getText() – The getText() method returns the text displayed on the alert box.
voidsendKeys(String stringToSend) – The sendKeys() method enters the specified string pattern into the alert box.

Syntax:
    Alert alert = driver.switchTo().alert();
	alert.accept();


15.	Mouse over
With the help of actions class, we can perform mouse over

Actions action = new Actions(webdriver);
WebElement we = webdriver.findElement(By.id("TextBox1"));
action.moveToElement(we).click().build().perform();

16.	Junit and testNG
Feature	JUnit 4	TestNG
test annotation	@Test	@Test
run before all tests in this suite have run	—	@BeforeSuite
run after all tests in this suite have run	—	@AfterSuite
run before the test	—	@BeforeTest
run after the test	—	@AfterTest
run before the first test method that belongs to any of these groups is invoked	—	@BeforeGroups
run after the last test method that belongs to any of these groups is invoked	—	@AfterGroups
run before the first test method in the current class is invoked	@BeforeClass	@BeforeClass
run after all the test methods in the current class have been run	@AfterClass	@AfterClass
run before each test method	@Before	@BeforeMethod
run after each test method	@After	@AfterMethod
ignore test	@ignore	@Test(enabled=false)
expected exception	@Test(expected = ArithmeticException.class)	@Test(expectedExceptions = ArithmeticException.class)
timeout	@Test(timeout = 1000)	@Test(timeout = 1000)


17.	Benefits of TestNGover Junit
There are number of benefits but from Selenium perspective, major advantages of TestNG are:
 1. It gives the ability to produce HTML Reports of execution
 2. Test cases can be Grouped & Prioritized more easily
 3. Parallel testing is possible
 4. Data Parameterization is possible


18.	Passing Parameters with DataProviders
@DataProvider(name = "test1")
public static Object[][] displayRollNumberAndName() {
	return new Object[][] { { 1, "Ravi" }, { 2, "Karan" }, { 3, "Divya" } };
}

@Test(dataProvider = "test1")
public void testPrimeNumberChecker(introllNumber, String name) {
	System.out.println("Roll number=" + rollNumber + " " + "Name=" + name);
}


19.	Listeners in testNG
There are many types of listeners which allows you to change the TestNG's behavior.
Below are the few TestNG listeners:
	1. IAnnotationTransformer
	2. IAnnotationTransformer2
	3. IConfigurable
	4. IConfigurationListener
	5. IExecutionListener
	6. IHookable
	7. IInvokedMethodListener
	8. IInvokedMethodListener2
	9. IMethodInterceptor
	10. IReporter
	11. ISuiteListener
	12. ITestListener
Above Interface are called TestNG Listeners. These interfaces are used in selenium to generate logs or customize the Testing reports.

I have used IReporter in my project. We have created on class which implements IReporter interface.
We have overridden generateReport method which takes three parameters.
Syntax:- public void generateReport(List<XmlSuite>xmlSuites, List<ISuite> suites, String outputDirectory)





20.	Run testing.xml from cmd
java -cp "path-tojar/testng.jar:path_to_yourtest_classes" org.testng.TestNG testng.xml


21.	Run testcase for multiple times in testng
@Test(invocationCount=10)
public void test() {
	System.out.println("Hi");
}


22.	Detect test failure in testng @AfterMethod
@AfterMethod
public void tearDown(ITestResult result) {
if (result.getStatus() == ITestResult.FAILURE) {
      //your screenshooting code goes here
   }        
}


23.	Test priority in testNG
In TestNG "Priority" is used to schedule the test cases. When there are multiple test cases, we want to execute test cases in order.
We need to add annotation as @Test(priority=??). The default value will be zero for priority.
If we define priority as "priority=", these test cases will get executed only when all the test cases which don't have any priority as the default priority will be set to "priority=0"


24.	Exception in test
In TestNG we use expectedException with @Test annotation and we need to specify the type of exceptions that are expected to be thrown when executing the test methods.
A below example which throws an exception called “ArithmeticException” when dividing two numbers with denominator value as 0.

@Test(expectedExceptions=ArithmeticException.class)
public void dividedByZeroExample1(){
	int e = 1/0;
}

If we remove the “(expectedException = ArithmeticException.class)”, it will return exception called “java.lang.ArithmeticException: / by zero”.



25.	Test

26.	Exceptions in Selenium WebDriver
What is an Exception?
"An Exception is an event, which occurs during the execution of a program that disrupts the normal flow of the program’s instructions or in simple words, any issue which makes your test case stop in between the execution."
 
When exception occurs, the normal flow of program halts & an exception object is created. The program then tries to find someone that can handle the raised exception. The exception object contains a lot of debugging information such as method hierarchy, line number where the exception occurred, type of exception etc. The process of creating the exception object and handing it over to run-time environment is called “throwing the exception”

Common Exceptions in Selenium WebDriver
There is a complete list of Exceptions in Selenium WebDriver mentioned in the Selenium Doc which you may or may not encounter in course of your testing. Hence in this article we will focus on some most common exceptions in Selenium WebDriver,

1.	ElementNotVisibleException: Although an element is present in the DOM, it is not visible (cannot be interacted with). E.g. Hidden Elements – defined in HTML using type=”hidden”.
2.	ElementNotSelectableException: Although an element is present in the DOM, it may be disabled (cannot be clicked/selected).
3.	InvalidSelectorException: Selector used to find an element does not return a WebElement. Say XPath expression is used which is either syntactically invalid or does not select WebElement.
4.	NoSuchElementException: WebDriver is unable to identify the elements during run time, i.e. FindBy method can’t find the element.
5.	NoSuchFrameException: WebDriver is switching to an invalid frame, which is not available.
6.	NoAlertPresentException: WebDriver is switching to an invalid alert, which is not available.
7.	NoSuchWindowException: WebDriver is switching to an invalid window, which is not available.
8.	StaleElementReferenceException: The referenced element is no longer present on the DOM page (reference to an element is now Stale). E.g. The Element belongs to a different frame than the current one OR the user has navigated away to another page.
9.	SessionNotFoundException: The WebDriver is performing the action immediately after ‘quitting’ the browser.
10.	TimeoutException: The command did not complete in enough time. E.g. the element didn’t display in the specified time. Encountered when working with waits.
11.	WebDriverException: The WebDriver is performing the action immediately after ‘closing’ the browser.

 


27.	Difference between xpath and cssselector
CSS selectors perform far better than Xpath and it is well documented in Selenium community. Here are some reasons,
	1. Xpath engines are different in each browser, hence make them inconsistent
	2. IE does not have a native xpath engine, therefore selenium injects its own xpath engine for compatibility of its API. Hence we lose the advantage of using native browser features that WebDriver inherently promotes.
	
Xpath search the element in backword as well as forword direction in DOM. That means we can find parent element from child element
CSS selector search the elementonly in forword direction.


28.	What is absolute and relative XPATH
i)	Absolute XPath - It is the direct way to find the element, but the disadvantage of the absolute XPath is that if there are any changes made in the path of the element then that XPath gets failed.
The key characteristic of XPath is that it begins with the single forward slash(/) ,which means you can select the element from the root node.

ii)	Relative XPath - Relative Xpath the path starts from the middle of the HTML DOM structure. It starts with the double forward slash (//), which means it can search the element anywhere at the webpage.


29.	Xpath and cssselector examples
CssSelector:-
In CSS there are two special characters which has important role to play.
1. dot(.) refers to class
	css=input.submitbtn
	Example:- driver.findElement(By.cssSelector("input.lst-ib")).sendKeys("Hello");
2. Hash(#) refers to Id
	css=input#destination
Example:-driver.findElement(By.cssSelector("input#lst-ib")).sendKeys("Hello");

Using CSS locators, we can also locate elements with sub-strings. Which are really help full when there are dynamically generated ids in webpage
	There are there important special characters:
	1. '^' symbol, represents the starting text in a string. Ex:-css=input[id^='ema']
	2. '$' symbol represents the ending text in a string. Ex:-css=input[id$='mail']
	3. '*' symbol represents contains text in a string. Ex:-css=input[id*='mai']
Example: - driver.findElement(By.cssSelector("input[id*='mai']")).sendKeys("Hello");
	
XPath: -
1) Basic XPath: - 
	//input[@name='uid']
	
2) Contains(): - 
	//div[contains(@type,'sub')]
	//*[contains(text(),'here')]
	//*[contains(.,'here')]
	
3) Using OR & AND: -
	//*[@type='submit' OR @name='btnReset']
	//input[@type='submit' AND @name='btnLogin']
4) Start-with function: -
	//label[starts-with(@id,'message')]
5) Text():-
	//td[text()='UserID']
6) XPath axes methods: - These XPath axes methods are used to find the complex or dynamic elements. Below we will see some of these methods.
	a) Following:- //*[@type='text']//following::input
	b) Ancestor:- //*[text()='Enterprise Testing']//ancestor::div
	c) Child:- //*[@id='java_technologies']/child::li
	d) Preceding:- //*[@type='submit']//preceding::input
	e) Following-sibling:- //*[@type='submit']//following-sibling::input
	f) Parent:- //*[@id='rt-feature']//parent::div
	g) Self:- //*[@type='password']//self::input
	h) Descendant:- //*[@id='rt-feature']//descendant::a



30.	Difference betweendriver.close() and driver.quit()

close() :- is a webdriver command which closes the browser window which is currently in focus.

During the automation process, if there are more than one browser window opened, then the close() command will close only the current browser window which is having focus at that time. The remaining browser windows will not be closed.

quit() is a webdriver command which calls the driver.dispose method, which in turn closes all the browser windows and terminates the WebDriver session. If we do not use quit() at the end of program, the WebDriver session will not be closed properly and the files will not be cleared off memory. This may result in memory leak errors.



31.	How to Double click on button/link in selenium
Actions action = new Actions(driver);
WebElement we=driver.findElement(By.xpath("html/body/div[1]"));
action.moveToElement(we).doubleClick().perform();

JavascriptExecutor:-







32.	Selenium grid

Selenium-Grid allows you run your tests on different machines against different browsers in parallel. That is, running multiple tests at the same time against different machines running different browsers and operating systems.

Starting a Hub: - To start a hub with default parameters, run the following command from a command-line. This will work on all the supported platforms, Windows Linux, or Mac OSX.

java -jar selenium-server-standalone-2.44.0.jar -role hub (Default port is 4444)
java -jar selenium-server-standalone-2.44.0.jar -role hub -port 4441

This starts a hub using default parameter values. 

Starting a Node:- To start a node using default parameters, run the following command from a command-line.

java -jar selenium-server-standalone-2.44.0.jar -role node  -hub http://localhost:4444/grid/register

33.	How to take screenshot in selenium

WebDriver driver = new FirefoxDriver();
driver.get("http://www.google.com/");
File scrFile = ((TakesScreenshot)driver).getScreenshotAs(OutputType.FILE);
FileUtils.copyFile(scrFile, new File("c:\\tmp\\screenshot.png"));

34.	Database connectivity

Process of connecting to a database and executing a query consist of the following:

1. Import JDBC packages.
	importjava.sql.*;

2. Load and register the JDBC driver.
	Class.forName("oracle.jdbc.driver.OracleDriver");
	or
	DriverManager.registerDriver(new oracle.jdbc.driver.OracleDriver());

3. Open a connection to the database.
	Connection conn = DriverManager.getConnection(URL, username, passwd);
	
4. Create a statement object to perform a query.
	Statement stmt = conn.createStatement();
	
5. Execute the statement object and return a query resultset.
	ResultSetrset = stmt.executeQuery("SELECT * FROM employee");
	or to delete/update/insert statement
	stmt.update("update student set username='Ravindra' where roleid=100");
	
6. Process the resultset.
	String str;
	while (rset.next())
		{
			str = rset.getInt(1)+ " "+ rset.getString(2)+ "\n";
		}

7. Close the resultset and statement objects.
	rset.close();
	stmt.close();

8. Close the connection.
	conn.close();


35.	Read data from property file
try {
		File file = new File("C:\\..\\test.properties");
		FileInputStreamfileInput = new FileInputStream(file);
		Properties properties = new Properties();
		properties.load(fileInput);
		fileInput.close();
			
		Set<Object> set= new HashSet<Object>();
		set=properties.keySet();

		Iterator<Object>itr=set.iterator();
			
		while (itr.hasNext()) {
			String key = (String) itr.next();
			String value = properties.getProperty(key);
			System.out.println(key + ": " + value);
		}
	} catch (Exception ex) {
			System.out.println("Exception");
	}


File file = new File("test.properties");
FileInputStreamfileInput = new FileInputStream(file);
Properties properties = new Properties();
properties.load(fileInput);
fileInput.close();

Enumeration enuKeys = properties.keys();
while (enuKeys.hasMoreElements()) {
	String key = (String) enuKeys.nextElement();
	String value = properties.getProperty(key);
	System.out.println(key + ": " + value);
 }


36.	Read data from XML file

XML Code:
<?xml version="1.0"?>
<company>
<staffid="1001">
<firstname>Ravindra</firstname>
<lastname>Jadhav</lastname>
<nickname>Ravi</nickname>
<salary>100000</salary>
</staff>
<staffid="2001">
<firstname>Karan</firstname>
<lastname>Sharma</lastname>
<nickname>Mahi</nickname>
<salary>200000</salary>
</staff>
</company>

try {
	File fXmlFile = new File("C:\\Selenium practice\\ReadXMLData.xml");
	DocumentBuilderFactorydbFactory = DocumentBuilderFactory.newInstance();
	DocumentBuilderdBuilder = dbFactory.newDocumentBuilder();
	Document doc = dBuilder.parse(fXmlFile);
	doc.getDocumentElement().normalize();

	System.out.println("Root element :" + doc.getDocumentElement().getNodeName());
	NodeListnList = doc.getElementsByTagName("staff");
	System.out.println("----------------------------");

	for (int temp = 0; temp <nList.getLength(); temp++) {
		Node nNode = nList.item(temp);
		System.out.println("\nCurrent Element :" + nNode.getNodeName());
	if (nNode.getNodeType() == Node.ELEMENT_NODE) {
		Element eElement = (Element) nNode;
		System.out.println("Staff id : " + eElement.getAttribute("id"));
		System.out.println("First Name : " + eElement.getElementsByTagName("firstname").item(0).getTextContent());
		System.out.println("Last Name : " + eElement.getElementsByTagName("lastname").item(0).getTextContent());
		System.out.println("Nick Name : " + eElement.getElementsByTagName("nickname").item(0).getTextContent());
		System.out.println("Salary : " + eElement.getElementsByTagName("salary").item(0).getTextContent());
			}
		}
	} catch (Exception e) {
		e.printStackTrace();
	}

37.	Read/Write data from excel file

Read Data from Excel file:-
//Create an object of File class to open xlsx file
File file = new File("C:\\Selenium practice\\ReadData.xlsx");

//Create an object of FileInputStream class to read excel file
FileInputStreaminputStream = new FileInputStream(file);

Workbook workbook = new XSSFWorkbook(inputStream);
	
//Read sheet inside the workbook by its name
Sheet sheet = workbook.getSheet("Sheet1");

//Find number of rows in excel file
introwCount = sheet.getLastRowNum() - sheet.getFirstRowNum();

//Create a loop over all the rows of excel file to read it
for (inti = 0; i< rowCount+1; i++) {
Row row = sheet.getRow(i);
System.out.println(row.getCell(0).getStringCellValue()+" || " + row.getCell(1).getStringCellValue());
       }
workbook.close();
inputStream.close();

Write Data in Excel file:-
//Create an object of File class to open xlsx file
File file = new File("C:\\Selenium practice\\ReadData.xlsx");

//Create an object of FileInputStream class to read excel file
FileInputStreaminputStream = new FileInputStream(file);
Workbook workbook = new XSSFWorkbook(inputStream);

//Read excel sheet by sheet name    
Sheet sheet = workbook.getSheet("sheet1");

//Get the current count of rows in excel file
introwCount = sheet.getLastRowNum()-sheet.getFirstRowNum();

//Get the first row from the sheet
Row row = sheet.getRow(0);

for(inti=100,k=1;i<110;i++,k++) {
	//Create a new row and append it at last of sheet
	Row newRow = sheet.createRow(rowCount+k);

	//Create a loop over the cell of newly created Row
	for(int j = 0; j <row.getLastCellNum(); j++){
        //Fill data in row
        Cell cell = newRow.createCell(j);
cell.setCellValue(i+j);
	  }
	}

//Close input stream
inputStream.close();

//Create an object of FileOutputStream class to create write data in excel file
FileOutputStreamoutputStream = new FileOutputStream(file);

//write data in the excel file
workbook.write(outputStream);

//close output stream
outputStream.close();

38.	Select class (dropdown)
Before we can control drop-down boxes, we must do following two things:

1. Import the package org.openqa.selenium.support.ui.Select
2. Instantiate the drop-down box as a "Select" object in WebDriver

importorg.openqa.selenium.support.ui.Select;

 Select dropdown = new Select(driver.findElement(By.id("SelectID_One")));

dropdown.selectByValue("greenvalue");
dropdown.selectByVisibleText("Lime");
dropdown.selectByIndex(2);  // Index starts with 0


39.	Scrolling in Selenium
A Scrollbar is a lets you move around screen in horizontal or vertical direction if the current page scroll does not fit the visible area of the screen. It is used to move the window up and down.

Selenium Webdriver does not require scroll to perform actions as it manipulates DOM. But in certain web pages, elements only become visible once the user have scrolled to them. In such cases scrolling may be necessary.

Let's, see the scroll down a web page using the selenium webdriver with following 3 scenarios:
Scenario 1: To scroll down the web page by pixel.
 Syntax: - JavascriptExecutorjs = (JavascriptExecutor) driver;
	  // this will scroll down the page by 1000 pixel vertical		
js.executeScript("window.scrollBy(0,1000)");
		
Scenario 2: To scroll down the web page by the visibility of the element.
 Syntax: - JavascriptExecutorjs = (JavascriptExecutor) driver;
	  //Find element by link text and store in variable "Element"        		
WebElement Element = driver.findElement(By.linkText("Linux"));
               //This will scroll the page till the element is found		
js.executeScript("arguments[0].scrollIntoView();", Element);
		
Scenario 3: To scroll down the web page at the bottom of the page.
 Syntax: -  JavascriptExecutorjs = (JavascriptExecutor) driver;
	    //This will scroll the web page till end.		
js.executeScript("window.scrollTo(0, document.body.scrollHeight)");
			
Scenario 4: Horizontal scroll on the web page. [Same as scenario 2]
 Syntax: -  JavascriptExecutorjs = (JavascriptExecutor) driver;
//This will scroll the page Horizontally till the element is found		js.executeScript("arguments[0].scrollIntoView();", Element);


40.	Framework types
A framework is a set of structure of the entire automation suit. It is also a guideline, if followed can result in a structure which is easy to maintain and enhance. These guidelines include:
 1. Coding standards
 2. Handling the test data
 3. Maintaining and handling the elements (object repository in QTP)
 4. Handling of environment files and properties file
 5. Reporting of data
 6. Handling logs

Different types of framework available are:
 1. Keyword driven framework
 2. Data Driven framework
 3. Hybrid Framework
 4. Behavior Driven Development Framework

1. Keyword driven framework
It is also known as table-driven testing or action word based testing. In Keyword-driven testing, we use a table format to define keywords or action words for each function or method that we would execute. It performs automation test scripts based on the keywords specified in the excel sheet. By using this Framework, testers can work with keywords to develop any test automation script, testers with less programming knowledge would also be able to work on the test scripts. The logic to read keywords and call the required action mentioned in the external excel sheet is placed in the main class.

2. Data Driven framework
Data driven test automation framework is focused on separating the test scripts logic and the test data from each other. Allows us to create test automation scripts by passing different sets of test data. The test data set is kept in the external files or resources such as MS Excel Sheets, MS Access Tables, SQL Database, XML files etc., the test scripts connect to the external resources to get the test data. By using this framework we could easily make the test scripts work properly for different sets of test data.

This framework gives more test coverage with reusable tests and flexibility in execution of tests only when required and by changing only the input test data and reliable in terms of no impact on tests by changing the test data but it has its own drawbacks such as testers who work on this framework needs to have hands-on programming knowledge to develop test scripts

3. Hybrid Framework
Hybrid Test automation framework is the combination of two or more frameworks mentioned above. It attempts to leverage the strengths and benefits of other frameworks for the particular test environment it manages.

4. Behavior Driven Development Framework
The purpose of this Behavior Driven Development framework is to create a platform which allows everyone (such as Business Analysts, Developers, Testers etc,) to participate actively. It requires increased collaboration between Development and Test Teams.  It doesn’t require the users to be acquainted with a programming language. We use non-technical, natural language to create test specifications. Some of the tools available in the market for Behavior Driven Development is JBehave, Cucumber, etc.,




41.	Desired Capabilities. 
What is Desired Capability?
 The desired capability is a series of key/value pairs that stores the browser properties like browsername, browser version, the path of the browser driver in the system, etc. to determine the behaviour of the browser at run time.

Desired capability can also be used to configure the driver instance of Selenium WebDriver.

Desired Capabilities are more useful in cases like:
	1. In mobile application automation, where the browser properties and the device properties can be set.
	2. In Selenium grid when we want to run the test cases on a different browser with different operating systems and versions.

Different types of Desired Capabilities Methods: -
	1. setBrowserName(java.lang.StringbrowserName)
	2. getBrowserName()
	3. setVersion(java.lang.String version)
	4. getVersion()
	5. setPlatform()
	6. getPlatform()
	7. setCapability()
	8. getCapability()

Capabilities for IE browser:-
  WebDriver driverObject=null;
System.setProperty("webdriver.ie.driver", "path" );   
DesiredCapabilities capabilities = DesiredCapabilities.internetExplorer();
capabilities.setCapability(InternetExplorerDriver.INTRODUCE_FLAKINESS_BY_IGNORING_SECURITY_DOMAINS, true);
driver = new InternetExplorerDriver(capabilities);

Capabilities for chrome browser:-
	1. Using the ChromeOptions class
		ChromeOptions options = new ChromeOptions();
		// Add the WebDriver proxy capability.
		Proxy proxy = new Proxy();
		proxy.setHttpProxy("myhttpproxy:3337");
		options.setCapability("proxy", proxy);

		// Add a ChromeDriver-specific capability.
		options.addExtensions(new File("/path/to/extension.crx"));
		ChromeDriver driver = new ChromeDriver(options);
	
	2. Using DesiredCapabilities
		cap = DesiredCapabilities.chrome();
		// options.setBinary(systemProperties);
		cap.setCapability(ChromeOptions.CAPABILITY, options);
		ChromeDriver driver = new ChromeDriver(cap);

Capabilities for Firefox browser: -
	FirefoxProfile profile = new FirefoxProfile();
	DesiredCapabilities dc=DesiredCapabilities.firefox();
	profile.setAcceptUntrustedCertificates(false);
	profile.setAssumeUntrustedCertificateIssuer(true);
	profile.setPreference("browser.download.folderList", 2);
	profile.setPreference("browser.helperApps.alwaysAsk.force", false);
profile.setPreference("browser.download.manager.showWhenStarting",false); profile.setPreference("browser.download.dir", "C:\Downloads"); profile.setPreference("browser.download.downloadDir","C:\Downloads"); profile.setPreference("browser.download.defaultFolder","C:\Downloads"); profile.setPreference("browser.helperApps.neverAsk.saveToDisk","text/anytext                               ,text/plain,text/html,application/plain" );
	dc = DesiredCapabilities.firefox();
	dc.setCapability(FirefoxDriver.PROFILE, profile);
	Webdriver driver =  newFirefoxDriver(dc);


42.	How to open firefox, chrome and IE on remote machine
DesiredCapabilities cap = null;
cap = DesiredCapabilities.firefox();
driver = new RemoteWebDriver("http://[Server_Name]:[port_number]/wd/hub", cap );


43.	Ways to refresh the browser
Following are the ways to refresh the web page:-
1) Refresh command: driver.navigate().refresh();
2) Get command: driver.get(driver.getCurrentUrl());
3) To command: driver.navigate().to(driver.getCurrentUrl());
4) SendKeys command: 
	i) driver.findElement(By.name("Any textbox")).sendKeys(Keys.F5);
ii) driver.findElement(By.name("Any textbox")).sendKeys("\uE035");


44.	Handling Dynamic web tables using selenium webdriver
WebDriver driverObject;
System.setProperty("webdriver.chrome.driver","G://chromedriver.exe");
driverObject= new ChromeDriver();
driverObject.get("http://money.rediff.com/gainers/bsc/dailygroupa?");         

 //No.of Columns
List  col = driver.findElements(By.xpath(".//*[@id=\"leftcontainer\"]/table/thead/tr/th"));
System.out.println("No of cols are : " +col.size()); 
 //No.of rows 
List  rows = driver.findElements(By.xpath(".//*[@id='leftcontainer']/table/tbody/tr/td[1]")); 
System.out.println("No of rows are : " + rows.size());

driverObject.close();


45.	

