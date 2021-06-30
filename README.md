This is the temperature conversion app
Pre-requisites:
1. VS Code
2. Visual Studio .Net 2015 plus

How to run the app
1. The package has angular code and .net solution
2. I have not updated the angular with ng modules Mat module and bootstrap compnents (as it is very huge) so you may have to put it in the directory. 3. Open the .net solution, build it and run it by pressing F5.
4. Keep the .net solution running and then open the Angular project directly in VS Code and run ng serve command

Code description for the front-end side
1. The code is a standard angular boiler plate code base with components
  a. About component (this one) and
  b. Temperature conversion app
2. The angular front end is run via ng serve command on standard 4200 port. 3. The routing module has the components defined.
4. I have used angular material buttons for basic navigation at the top
5. I have used form validation for validating the input on the front end to make sure the user is entering a valid number or decimal.
6. I have hooked up bootstrap to be the app's main css by changing the angular.json file.
7. I have made the re-usable component "error-details" to be used for all the input fields of celsius, fahrenheit and kelvin.
8. App logic is simple meaning the user can enter value in any of the three fields and click the button beside that field to get the conversion for the rest of the two fields
   for eg, the user can enter value in celsius text box and click the button beside it to get the fahrenheit and kelvin value for that celsius value

Code description for the back-end side
1. The backend code is a standard .net webapi web application again with some boiler plate code.
2. I have made some changes in the WebApiConfig.cs file of the project to hook up 4200 port for cross origin requests(CORS).
3. I have also set the jsonFormatter as the default one for the http requests and responses and removed the xml formatter in the same file.
4. I have created a new controller called as TemperatureConvertController and it has a single method to take the httppost temperature object and return the same type of object but after temperature conversion it.
5. I have created a basic business logic layer(BLL) which does the conversion into different formats.
6. I have created a static extension method class to convert the various inputs to targetted desired outputs.
7. I have created some unit test cases as well in the .net solution using Fake it easy and nUnit nuget packages.
