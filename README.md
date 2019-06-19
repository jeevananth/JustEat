# JustEat 

 

This source uses Java8 with Maven, Selenium and Cucumber stack.

The runner for this project is JUnit



# Prerequisites



- Install JDK8 and setup environment variables

- Install maven and setup path variable

-Eclipse Users : Download the plugin Natural(0.76) from Eclipse Marketplace. Thsi will work only in Eclipse Oxygen version



# Usage



- Setup browser driver location path of your local machine in 

   setProperties() method of src/test/java/com/pages/BasePage.java class



- Runner class is /src/test/java/com/runnermap/CucumberRunner.java. run this test case as a JUnit test case

- Before running make sure all your artifacts are downloaded from maven repository



# Description



- There are 3 scenarios for the given feature.

   1.Verify restuarant search results for valid pincode

      This scenario is tested by entering a valid pin code and asserted if the result renders value

   

   2.Verify restuarant search results for invalid pincode	 

      This scenario is tested by entering 4 different combinations of invalid pincode and the correspoding error message is verified. 

	

   3.Verify restuarant search results for invalid pincode

      This scenario is tested by entering a valid pincode which does not ahve any open/available restaurants



# Flow



The Scenario flow starts with the CucumberRunner.Java Class. 

- Once run is clicked, it checks for a @Before annotation. @Before instatiates the browser driver and wait element

- The next flow to be implemented is the @Given .The corresponding step definition will navigate to the Just Eats landing page and will check if the user is in that page

- The next implementation will enter a postal code and submit the entered code

- The next step will check if the user is navigated to search results page in the case when he netered a valid postal code or will check for an error message in the case when user entered an invalid postal code

- Finally the after annotation which will delete all the driver instances and close the browser.
