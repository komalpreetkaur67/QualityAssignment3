# QualityAssignment3
public void InvalidPostalCodeField()
        {
            IWebDriver webDriver = new ChromeDriver(@"D:\SEM 4");

            webDriver.Navigate().GoToUrl("file:///D:/SEM%204/SOFTWARE%20QUALITY/Assignment%203/index.html");

            IWebElement linkNewVehicle = webDriver.FindElement(By.LinkText("Enter new vehicle"));

            linkNewVehicle.Click();
            webDriver.FindElement(By.Name("sname")).SendKeys("Komalpreet");
            webDriver.FindElement(By.Name("lname")).SendKeys("Kaur");
            webDriver.FindElement(By.Name("address")).SendKeys("160 Gray Street");
            webDriver.FindElement(By.Name("city")).SendKeys("Kitchener");
            webDriver.FindElement(By.Name("province")).SendKeys("Ontario");
            webDriver.FindElement(By.Name("postal")).SendKeys("N2A3P7");
            webDriver.FindElement(By.Name("phone")).SendKeys("226-972-8471");
            webDriver.FindElement(By.Name("email")).SendKeys("Komalpreet7901@gmail.com");
            webDriver.FindElement(By.Name("vehicle")).SendKeys("BMW");
            webDriver.FindElement(By.Name("model")).SendKeys("Series 4");
            webDriver.FindElement(By.Name("year")).SendKeys("2021");

            webDriver.FindElement(By.XPath("//input[@value='Submit']")).Submit();
            Assert.Pass();

        }
        This test is for invalid Postal Code
