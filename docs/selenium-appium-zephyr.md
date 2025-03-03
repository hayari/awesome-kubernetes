# Test Automation Frameworks and Behavior Driven Development. Selenium, Cucumber, Appium & Zephyr Jira Plugin
- [Introduction](#introduction)
- [Selenium](#selenium)
- [Robot Framework](#robot-framework)
- [Cypress](#cypress)
- [Mobile Tests](#mobile-tests)
	- [Appium](#appium)
	- [Cucumber and Appium. Behavior Driven Development](#cucumber-and-appium-behavior-driven-development)
- [Test Automation with Zephyr (Jira Plugin)](#test-automation-with-zephyr-jira-plugin)

## Introduction
- [opensource.com: 9 open source test-automation frameworks](https://opensource.com/article/20/7/open-source-test-automation-frameworks) Get some advice to choose the right test-automation framework for your organization.

## Selenium
- [selenium.dev](https://selenium.dev/)
- [Dzone: what is selenium, getting started](https://dzone.com/articles/what-is-selenium-getting-started-with-selenium-aut)
- [Dzone: selenium tutorial for beginners](https://dzone.com/articles/selenium-tutorial-for-beginners-2)
- [Dzone: discover the top tips and tricks of selenium](https://dzone.com/articles/discover-the-top-tips-and-tricks-of-the-selenium-w)
- [Dzone: best practices for selenium automation](https://dzone.com/articles/best-practices-for-selenium-automation-one-must-kn)
- [Dzone: top 11 challenges in autmation testing using selenium](https://dzone.com/articles/top-11-challenges-in-automation-testing-using-sele)
- [youtube: execution test Selenium + Grafana + Jenkins](https://www.youtube.com/watch?v=vDj5IsWjU0A)
- [lambdatest.com: Why Selenium Grid Is Ideal For Automated Browser Testing?](https://www.lambdatest.com/blog/why-selenium-grid-is-ideal-for-automated-browser-testing/)
- [lambdatest.com: Top 27 Best Practices For Selenium Test Automation](https://www.lambdatest.com/blog/27-best-practices-selenium-test-automation/)
- [automationreinvented.blogspot.com: Top 30 Interview Questions on Automation Testing - Selenium for SDET/Automation QA?](https://automationreinvented.blogspot.com/2020/06/top-30-interview-questions-on.html)
- [lambdatest.com: Complete Guide To Access Forms In Selenium With Java](https://www.lambdatest.com/blog/complete-guide-to-access-forms-in-selenium-with-java/)
- [lambdatest.com: Selenium IDE: What Is It? & Why Is It Must For Every QA?](https://www.lambdatest.com/blog/selenium-ide-what-is-it-why-is-it-must-for-every-qa/)
- [qautomation.blog: How to run selenium script in JMeter](https://qautomation.blog/2019/05/07/how-to-run-selenium-script-in-jmeter/)
- [dev.to: Using Selenium With Python in a Docker Container](https://dev.to/nazliander/using-selenium-within-a-docker-container-ghp)
- [intellipaat.com: Selenium Tutorial – Learn Selenium from Experts](https://intellipaat.com/blog/tutorial/selenium-tutorial/)
- [lambdatest.com: How To Integrate Jenkins & Maven With Selenium?](https://www.lambdatest.com/blog/selenium-maven-jenkins-integration/)
- [lambdatest.com: Selenium 4 🌟](https://www.lambdatest.com/learning-hub/selenium-4)
- [automationreinvented.blogspot.com: How to run selenium tests from Jenkins? Maven and Jenkins Integration with Testng-Selenium? Run selenium maven project from command line? 🌟](https://automationreinvented.blogspot.com/2021/02/how-to-run-test-selenium-tests-from.html)
- [lambdatest.com/selenium: Introduction to Selenium Basics](https://www.lambdatest.com/selenium) Selenium is an open-source software to automate web testing by controlling browsers
based on your test scripts.
- [lambdatest.com: Selenium Webdriver Java Tutorial – Guide for Beginners](https://www.lambdatest.com/blog/selenium-java-tutorial-how-to-test-login-process/)
- [lambdatest.com: Complete Guide To Selenium Testing with GitHub Actions 🌟](https://www.lambdatest.com/blog/selenium-github-actions-example/)
- [lambdatest.com: 49 Most Common Selenium Exceptions for Automation Testing](https://www.lambdatest.com/blog/49-common-selenium-exceptions-automation-testing/)
- [lambdatest.com: How to execute JUnit 4 tests with JUnit 5 [Tutorial]](https://www.lambdatest.com/blog/execute-junit4-tests-with-junit5/)
- [lambdatest.com: How To Run Selenium Tests In Docker ? 🌟](https://www.lambdatest.com/blog/run-selenium-tests-in-docker/)
- [lambdatest.com: What Is New In Selenium 4 And What Is Deprecated In It? 🌟](https://www.lambdatest.com/blog/what-is-deprecated-in-selenium4/)
- [lambdatest.com: How To Upgrade From Selenium 3 To Selenium 4?](https://www.lambdatest.com/blog/upgrade-from-selenium3-to-selenium4/)
- [lambdatest.com: Automation Testing with Selenium JavaScript [Tutorial]](https://www.lambdatest.com/blog/automation-testing-with-selenium-javascript/)
- [lambdatest.com: How To Scroll a Page Using Selenium WebDriver?](https://www.lambdatest.com/blog/scroll-a-webpage-in-selenium-using-java/)
- [automationscript.com: Parallel Execution In Selenium Using Jenkins](https://automationscript.com/parallel-execution-in-selenium-using-jenkins/)
- [lambdatest.com: How To Modify HTTP Request Headers In JAVA Using Selenium WebDriver?](https://www.lambdatest.com/blog/modifying-http-request-headers-in-java-using-selenium-webdriver)
- [dzone: What's New in Selenium 4?](https://dzone.com/articles/what-is-new-in-selenium-4) The newly released Selenium 4 is creating a lot of buzz and the complete testing community is looking forward to exploring its updated features.
- [freecodecamp.org: Use Selenium to Create a Web Scraping Bot](https://www.freecodecamp.org/news/use-selenium-to-create-a-web-scraping-bot)
- [lambdatest.com: Debunking The Top 8 Selenium Testing Myths](https://www.lambdatest.com/blog/debunking-selenium-testing-myths/)
- [linkedin.com: Selenium 4 and Grid Integration with Kubernetes 🌟](https://www.linkedin.com/pulse/selenium-4-grid-integration-kubernetes-rishi-khanna/) This article is written to highlight Selenium 4 capabilities and how selenium grid can be incorporated with Kubernetes.

## Robot Framework
* [Robot Framework 🌟](https://robotframework.org/) Robot Framework is a generic open source automation framework. It can be used for test automation and robotic process automation (RPA).

## Cypress
- [lambdatest.com: Selenium vs Cypress – Which Is Better in 2021?](https://www.lambdatest.com/blog/cypress-vs-selenium-comparison/)

## Mobile Tests
### Appium
- [appium.io](http://appium.io/)
- [Dzone: appium tutorial for complete beginners](https://dzone.com/articles/appium-tutorial-for-complete-beginners)
- [Dzone: best practices in appium](https://dzone.com/articles/best-practices-in-appium)

### Cucumber and Appium. Behavior Driven Development
- [experitest.com: Start Automating your mobile tests with Cucumber and Appium](https://experitest.com/appium-blog/start-automating-your-mobile-tests-with-cucumber-and-appium/)
- [medium: Testing APIs with Python 🌟](https://medium.com/python-in-plain-english/testing-apis-with-python-4ca51d604ffe) Getting started with BDD, Cucumber, and Gherkin.
- [lambdatest.com: How To Integrate Cucumber With Jenkins?](https://www.lambdatest.com/blog/cucumber-with-jenkins-integration)
- [tutorials.virtualan.io: Idaithalam - Lowcode Test Automation](https://tutorials.virtualan.io/#/Idaithalam) Low code Test automation framework using cucumber and supports Behavior Driven Development (BDD). Can build test cases using Excel and Postman collection. It allows to build and test api workflow in minutes.
- [testinglpoint.com: Cucumber Interview Question](https://www.testinglpoint.com/cucumber-interview-question/)
- [dzone: API Testing With Cucumber](https://dzone.com/articles/api-testing-with-cucumber) Testing APIs in a microservices environment can be a challenging task. In this tutorial, we will learn to address it in BDD-style testing using Cucumber.

## Test Automation with Zephyr (Jira Plugin)
- [Atlassian Marketplace: Zephyr](https://marketplace.atlassian.com/apps/1014681/zephyr-for-jira-test-management)
- [Dzone: 14 of the best automation testing tools available](https://dzone.com/articles/14-of-the-best-automation-testing-tools-available)
- [Dzone: Find the best agile testing tools for your team](https://dzone.com/articles/find-the-best-agile-testing-tools-for-your-team)
- [Dzone: Zephyr for Jira cloud](https://dzone.com/articles/zephyr-for-jira-cloud-june-release-is-here)
- [Dzone: The power of automated testing and test management](https://dzone.com/articles/the-power-of-automated-testing-and-test-management)
- [Dzone: A Jira tutorial for software developers](https://dzone.com/articles/a-jira-tutorial-for-software-developers-get-the-mo)
