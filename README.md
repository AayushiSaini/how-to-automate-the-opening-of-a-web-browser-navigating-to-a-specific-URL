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
#Automating interactions on the LambdaTest website:
package org.example;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeOptions;
import org.openqa.selenium.remote.RemoteWebDriver;
import java.net.URL;

public class standalone {
    public static void main(String[] args) {
        ChromeOptions chromeOptions = new ChromeOptions();
        chromeOptions.setCapability("platformName", "windows");
        
        try {
            WebDriver driver = new RemoteWebDriver(new URL("http://192.168.100.177:4444"), chromeOptions);
            driver.get("https://accounts.lambdatest.com/login");
            driver.findElement(By.xpath("//*[@id=\"email\"]")).sendKeys("aayushis@lambdatest.com");
            driver.findElement(By.xpath("//*[@id=\"password\"]")).sendKeys("123456");
            driver.findElement(By.xpath("//*[@id=\"login-button\"]")).click();

            // Open the signup page
            driver.get("https://accounts.lambdatest.com/register");
            driver.findElement(By.xpath("//*[@id=\"email\"]")).sendKeys("aayushis@lambdatest.com");

            driver.findElement(By.xpath("//*[@id=\"userpassword\"]")).sendKeys("123456");
            driver.findElement(By.xpath("//*[@id=\"app\"]")).click();
            driver.get("https://www.instagram.com/accounts/login/?hl=en");
            driver.findElement(By.xpath("//*[@id=\"loginForm\"]/div/div[1]/div/label/input")).sendKeys("aayushis@lambdatest.com");



            System.out.println("Page title is: " + driver.getTitle());
            Thread.sleep(10000);
            driver.quit();
        }
        catch (Exception e) {
            e.printStackTrace();

        }
    }
}
nput")).sendKeys("aayushis@lambdatest.com");

