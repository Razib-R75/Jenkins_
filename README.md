# Jenkins Pipeline Project with Maven Java Selenium Automation

This project demonstrates how to integrate a Maven Java Selenium automation code into a Jenkins Pipeline project.

## Overview

This repository contains a Maven project with Java code for Selenium automation testing. The tests are configured to run using Maven and Selenium, and the project is integrated into a Jenkins Pipeline for continuous integration.

## Getting Started

To get started with this project, follow these steps:

1. **Clone the Repository**: 
git clone https://github.com/Razib-R75/Jenkins_Pipeline.git

markdown
Copy code

2. **Set Up Jenkins**: 
- Make sure you have Jenkins installed and running.
- Install necessary plugins for Maven and Git integration.

3. **Create Jenkins Pipeline Project**:
- Create a new Pipeline project in Jenkins.
- Configure the pipeline to point to your Git repository.

4. **Configure Pipeline**: 
- Configure the pipeline script to execute the Maven commands for building and running the tests.
- Example Pipeline script:
  ```groovy
  pipeline {
      agent any
      
      stages {
          stage('Build') {
              steps {
                  sh 'mvn clean install'
              }
          }
          stage('Test') {
              steps {
                  sh 'mvn test'
              }
          }
      }
  }
  ```

5. **Run the Pipeline**: 
- Trigger the pipeline manually or set up a webhook for automatic triggering on code changes.

## Project Structure

The project structure is as follows:

- **src/main/java**: Contains the main Java source code for the Selenium automation.
- **src/test/java**: Contains the test classes for Selenium automation testing.
- **pom.xml**: Maven project configuration file with dependencies and plugins.

## Dependencies

This project has the following dependencies:

- Java Development Kit (JDK)
- Maven
- Selenium WebDriver
- WebDriverManager

## Contributing

Contributions to this project are welcome. Feel free to open issues or pull requests for any improvements or fixes.

## License

This project is licensed under the [MIT License](LICENSE).
