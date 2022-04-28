# calculator1
	import java.util.concurrent.TimeUnit;
	import org.openqa.selenium.By;
	import org.openqa.selenium.WebDriver;
	import org.openqa.selenium.chrome.ChromeDriver;
	import org.testng.annotations.AfterTest;
	import org.testng.annotations.BeforeTest;
	import org.testng.annotations.Test;

	public class Caltest {
	
		public WebDriver driver;
			
				@BeforeTest
				public void Setup1()
				{
					System.setProperty("Webdriver.chrome.driver", "C:\\Users\\Admin\\Desktop\\SeleniumComponents\\cd.exe");
				   driver= new ChromeDriver();
				   
					driver.manage().window().maximize();
					driver.manage().timeouts().pageLoadTimeout(2000,TimeUnit.SECONDS);
					driver.manage().timeouts().implicitlyWait(20,TimeUnit.SECONDS);
					driver.manage().deleteAllCookies();
					driver.get("https://www.calculator.net/ ");
					
				}
				
				@Test(priority=3)
				public void multiplication() throws Exception 
				{
					
					
			    driver.findElement(By.xpath("//span[contains(text(),'4')]")).click();
			  
			   driver.findElement(By.xpath("//span[contains(text(),'2')]")).click();
			   driver.findElement(By.xpath("//span[contains(text(),'3')]")).click();
			    driver.findElement(By.xpath("//span[contains(text(),'×')]")).click();
			    driver.findElement(By.xpath("//span[contains(text(),'5')]")).click();
			    driver.findElement(By.xpath("//span[contains(text(),'2')]")).click();
			    driver.findElement(By.xpath("//span[contains(text(),'5')]")).click();
			    driver.findElement(By.xpath("//span[contains(text(),'=')]")).click();
			    Thread.sleep(2000);

			    System.out.println("Ans of Multiplication 222075");
			
				}
				
				@Test(priority=4)
				public void div() throws Exception
				
				{
					 driver.findElement(By.xpath("//span[contains(text(),'4')]")).click();
					
					   driver.findElement(By.xpath("//tbody/tr[2]/td[2]/div[1]/div[4]/span[1]")).click();
					   driver.findElement(By.xpath("//tbody/tr[2]/td[2]/div[1]/div[4]/span[1]")).click();
					   driver.findElement(By.xpath("//tbody/tr[2]/td[2]/div[1]/div[4]/span[1]")).click();
					   driver.findElement(By.xpath("//tbody/tr[2]/td[2]/div[1]/div[4]/span[4]")).click();
					   driver.findElement(By.xpath("//span[contains(text(),'2')]")).click();
					   driver.findElement(By.xpath("//tbody/tr[2]/td[2]/div[1]/div[4]/span[1]")).click();
					   driver.findElement(By.xpath("//tbody/tr[2]/td[2]/div[1]/div[4]/span[1]")).click();
					   driver.findElement(By.xpath("//span[contains(text(),'=')]")).click();
					     Thread.sleep(2000);
					   System.out.println("Ans of Div 20");
				}
				
				@Test(priority=1)
				public void add() throws Exception
				{
					 driver.findElement(By.xpath("//span[contains(text(),'–')]")).click();
					 driver.findElement(By.xpath("//span[contains(text(),'2')]")).click();
					 driver.findElement(By.xpath("//span[contains(text(),'3')]")).click();
					 driver.findElement(By.xpath("//span[contains(text(),'4')]")).click();
					 driver.findElement(By.xpath("//span[contains(text(),'2')]")).click();
					 driver.findElement(By.xpath("//span[contains(text(),'3')]")).click();
					 driver.findElement(By.xpath("//span[contains(text(),'4')]")).click();
					 driver.findElement(By.xpath(" //tbody/tr[2]/td[2]/div[1]/div[1]/span[4]")).click();
					 driver.findElement(By.xpath("//span[contains(text(),'3')]")).click();
					 driver.findElement(By.xpath("//span[contains(text(),'4')]")).click();
					 driver.findElement(By.xpath("//span[contains(text(),'5')]")).click();
					 driver.findElement(By.xpath("//span[contains(text(),'3')]")).click();
					 driver.findElement(By.xpath("//span[contains(text(),'4')]")).click();
					 driver.findElement(By.xpath("//span[contains(text(),'5')]")).click();
					 driver.findElement(By.xpath("//span[contains(text(),'=')]")).click();
					 Thread.sleep(2000);
					 System.out.println("Ans of Add 111111");
					}
				
				@Test(priority=2 )   
				public void sub() throws Exception
				{
				 driver.findElement(By.xpath("//span[contains(text(),'2')]")).click();
				   driver.findElement(By.xpath("//span[contains(text(),'3')]")).click();
				   driver.findElement(By.xpath("//span[contains(text(),'4')]")).click();
			driver.findElement(By.xpath("//span[contains(text(),'8')]")).click();
				   driver.findElement(By.xpath("//span[contains(text(),'2')]")).click();
				   driver.findElement(By.xpath("//span[contains(text(),'3')]")).click();
				   driver.findElement(By.xpath("//span[contains(text(),'–')]")).click();
				   driver.findElement(By.xpath("//span[contains(text(),'–')]")).click();
				   driver.findElement(By.xpath("//span[contains(text(),'2')]")).click();
				   driver.findElement(By.xpath("//span[contains(text(),'3')]")).click();
				   driver.findElement(By.xpath("//tbody/tr[2]/td[2]/div[1]/div[4]/span[1]")).click();
				   driver.findElement(By.xpath("//span[contains(text(),'9')]")).click();
				   driver. findElement(By.xpath("//span[contains(text(),'4')]")).click();
				   driver.findElement(By.xpath("//span[contains(text(),'8')]")).click();
				   driver.findElement(By.xpath("//span[contains(text(),'2')]")).click();
				   driver.findElement(By.xpath("//span[contains(text(),'3')]")).click();
				   driver.findElement(By.xpath("//span[contains(text(),'=')]")).click();

				   Thread.sleep(2000);
						System.out.println("Ans ofsub23329646");
				}
				
				@AfterTest
				public void close1() 
				{
		driver.close();
				}
