## Exception Handling

### G4C Mini Project from November 27th

This is a Spring MVC Project to practice Exception Handling. The following was provided:

* An HTML page with appropriate forms and mustache markup
* A Controller with appropriate Get and Post Mappings

The goal for the assignment was to handle common exceptions without serving an HTTP 500 to the user.

The following exceptions were handled using try/ catch blocks:

* StringIndexOutOfBoundsException
* NumberFormatException (two examples)
* DateTimeException
* MalformedURLException

Some "Gotchas":

* In the StringIndexOutOfBoundsException example, the provided code only displayed the characters entered after the 4th position. This was fixed by having the Try block run the following, which added the full String "probablySomeText" to the view if the condition was met:

```			
probablySomeText.substring(4);
mv.addObject("stringResult", probablySomeText); 

```

* In the URLResult, the mustache is wrapped in an anchor href, so setting your view to URLFailure fixed this issue
* Entering a whole number in the Decimal field converts the String to a Double, so NumberFormatException is thrown 