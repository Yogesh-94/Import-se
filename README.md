
# QA Framework Utilities

This repository contains the **QA framework JAR** (`kellton_qa_framework-0.0.1-SNAPSHOT.jar`) and its **documentation (`index.html`)** for Selenium/Java automation projects.

---

## Folder Structure

your-project/
├─ src/ # Source code
├─ libs/ # External JARs
│ └─ kellton_qa_framework-0.0.1-SNAPSHOT.jar
├─ docs/ # Documentation
│ └─ index.html
├─ pom.xml or build.gradle # Build file (if Maven/Gradle)
└─ README.md


---

## Adding the JAR to Your Project

### IntelliJ IDEA
1. Right-click on the project → `Open Module Settings`.
2. Go to `Libraries` → `+` → Select `libs/kellton_qa_framework-0.0.1-SNAPSHOT.jar`.
3. The classes and methods will now be available for auto-suggestions in your code.

### Eclipse
1. Right-click on the project → `Build Path` → `Add External JARs`.
2. Select `libs/kellton_qa_framework-0.0.1-SNAPSHOT.jar`.
3. The classes and methods will now be available in your project.

### Maven (Optional)
If you want to use it as a Maven dependency locally:

```bash
mvn install:install-file \
  -Dfile=libs/kellton_qa_framework-0.0.1-SNAPSHOT.jar \
  -DgroupId=com.qa \
  -DartifactId=qa-utils \
  -Dversion=0.0.1-SNAPSHOT \
  -Dpackaging=jar

  
Then add this dependency in pom.xml:
 <dependency>
  <groupId>com.qa</groupId>
  <artifactId>qa-utils</artifactId>
  <version>0.0.1-SNAPSHOT</version>
</dependency>
 Accessing Documentation

Open docs/index.html in a browser to see a list of all BasePage utility methods with usage hints.

Brief method descriptions are also available in Javadoc inside the classes for IDE auto-suggestion

Quick Reference (Common Methods)
| Method                                                  | Description                                         |
| ------------------------------------------------------- | --------------------------------------------------- |
| `clickElement(WebElement element)`                      | Waits for the element to be clickable and clicks it |
| `enterText(WebElement element, String text)`            | Enters text into an input field                     |
| `scrollToElement(WebElement element)`                   | Scrolls the page to the given element               |
| `isElementVisible(WebElement element)`                  | Checks if an element is visible                     |
| `selectDropdownByText(WebElement element, String text)` | Selects a dropdown option by visible text           |

For the full list of methods and detailed documentation, refer to docs/index.html.

Notes

Always pull the latest version of the repository to get updates to the JAR or documentation.

If you add new utility methods, update both the JAR and index.html.

  
  