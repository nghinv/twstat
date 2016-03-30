the command to run the testsuite is:

java -jar selenium-server-standalone-2.45.0.jar -userExtensions user-extensions.js -htmlSuite "*firefox" "http://si-staging.mistral12.com/" "/home/filippo/selenese_extensions/test/suite.html" "/home/filippo/selenese_extensions/test/results.html" [Optional: -debug &> debug.log]


The file user-extensions.js contains our own script to read the summary table of SI, 
plus the code of sideflow.js, which is the .js version of "Selenium IDE: Flow Control" 
[https://addons.mozilla.org/it/firefox/addon/flow-control/]. 
The code of sideflow.js has been modified to allow 
selenium-server-standalone-2.45.0.jar to run it, 
because a discrepancy between the selenium server and seleniumIDE: 
*testCase.commands* 
should be replaced with *htmlTestRunner.currentTest.htmlTestCase.commandRows*


