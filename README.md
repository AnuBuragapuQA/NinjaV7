SeleniumHybridAutomationFramework is an enterprise-grade Java-based test automation framework designed to automate CloudBerry Store (OpenCart) application using a hybrid approach. This framework follows real-world industry standards and combines the strengths of Data-Driven and Page Object Model (POM) frameworks to deliver scalable, maintainable, and reusable test automation without using BDD/Cucumber. This framework supports cross-browser testing, parallel execution, and easy integration with CI/CD tools.

🛠️ Tech Stack
Programming Language: Java
Automation Tool: Selenium WebDriver
Test Framework: TestNG
Build Tool: Maven
Design Pattern: Page Object Model (POM)
Logging: Log4j
Version Control: Git & GitHub
CI Ready: Jenkins compatible
Reporting: TestNG Reports / Extent Reports
Browser Support: Chrome, Firefox, Edge
📂 Project Structure

│
│├── src/test/java
│   ├── pageobjects
│   │   └── Page Object classes representing application screens
│   │
│   ├── testbase
│   │   └── Base classes for WebDriver setup, browser initialization,
│   │       configuration loading, and common test setup/teardown
│   │
│   ├── testcases
│   │   └── TestNG test classes containing test scenarios
│   │
│   └── utilities
│       ├── DataProviders.java        → TestNG data providers
│       ├── ExcelUtility.java         → Read/write test data from Excel
│       ├── ExtentReportManager.java  → Extent report configuration
│       └── RetryAnalyzer.java        → Retry failed test cases
│
├── src/test/resources
│   ├── config.properties             → Environment & browser configuration
│   └── log4j2.xml                     → Logging configuration
│
├── logs
│     └── automation-YYYY-MM-DD.log     → Execution logs
│
├── reports
│   ├── Test-Report-YYYY.MM.DD.html   → Extent HTML reports
│
├── screenshots
│   └── Screenshots captured on test failure
│
├── testData
│   └── External test data files (Excel)
│
├── test-output
│   └── TestNG default reports
│
├── pom.xml                            → Maven dependencies & plugins
├── testng.xml                         → TestNG suite configuration
├── run.bat                            → Batch file to execute tests
└── README.md```


🚀 Features

Hybrid framework (POM + Data-Driven + utilities + TestNG)
Reusable Page Objects
Cross-browser testing support
Parallel execution using TestNG
Centralized configuration management
Reusable utility methods
Data-driven testing support
Maven-based dependency management
TestNG annotations & grouping
Jenkins CI integration
Scalable and easy to maintain

⚙️ Prerequisites

Make sure the following are installed:
Java (JDK 8 or above)
Maven
Git
Chrome / Firefox browsers
IDE (IntelliJ / Eclipse)

▶️ How to Run Tests
Run from command line
mvn clean test

Run using TestNG
Open testng.xml

Right-click → Run as TestNG Suite

🔹 Run by TestNG Groups
<groups>
  <run>
    <include name="sanity"/>
  </run>
</groups>
🔹 Parallel Execution
<suite parallel="tests" thread-count="3">

🔧 Configuration

All environment-specific values are maintained in the configuration file:
src/test/resources/config/config.properties
Example:
browser=chrome
url=https://example.com
implicitWait=10

📊 Reports
After execution, test reports can be found in:
/reports

Screenshots: Captured automatically on test failure

🌐 Application Under Test
CloudBerry Store (OpenCart)
https://www.cloudberrystore.services


🔄 CI/CD Integration
This project can be easily integrated with Jenkins for continuous testing:
Pull code from GitHub
Trigger builds on commit
Execute Maven goals
Publish test reports

🧩 Future Enhancements
CI/CD integration with Jenkins
Selenium Grid / Docker support
Cloud execution (BrowserStack / Sauce Labs)
API automation integration

👤 Author
Annapurna Buragapu
Software Test Engineer | Automation QA

⭐ Support
If you find this framework useful, give the repository a ⭐ and feel free to fork it.
