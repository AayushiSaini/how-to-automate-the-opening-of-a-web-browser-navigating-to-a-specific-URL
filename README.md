# How-to-Automate-the-opening-of-a-web-browser-navigating-to-a-specific-URL
This Java code snippet demonstrates how to automate the opening of a web browser, navigating to a specific URL, and printing the title of the webpage using Selenium WebDriver with the ChromeDriver.

Explanation:
Import WebDriver and ChromeDriver Classes:

The org.openqa.selenium.WebDriver and org.openqa.selenium.chrome.ChromeDriver classes are imported to use Selenium WebDriver and ChromeDriver functionalities.
Set ChromeDriver Path:

System.setProperty("webdriver.chrome.driver", "path/to/chromedriver.exe"); sets the system property to specify the path to the ChromeDriver executable file.
Initialize WebDriver:

WebDriver driver = new ChromeDriver(); initializes a new instance of the ChromeDriver, which will automate interactions with the Chrome browser.
Open a Website:

driver.get("https://www.google.com"); navigates the Chrome browser to the specified URL (in this case, Google's homepage).
Print Page Title:

System.out.println("Page title is: " + driver.getTitle()); retrieves and prints the title of the webpage opened in the browser.
Close the Browser:

driver.quit(); closes the browser window and ends the WebDriver session.
This code snippet demonstrates a basic Selenium WebDriver script using ChromeDriver to open a webpage and print its title. Make sure to replace the path to the ChromeDriver executable with the correct path on your local system.


