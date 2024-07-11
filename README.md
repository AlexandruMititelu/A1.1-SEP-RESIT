# Report for Assignment 1 Resit

## Project chosen

Name: Zod

URL: https://github.com/colinhacks/zod

Number of lines of code and the tool used to count it: 410107, lizard

Programming language: TypeScript

## Coverage measurement with existing tool

Name of the tool: jslint

Command: `$ yarn test --coverage   `

Screenshot of result, overall coverage:<br/>
![alt text](Photos/OG_coverage.png)
Screenshot of result, overall coverage of the file we are going to modify:<br/>
![alt text](Photos/OG_coverage2.png)


## Coverage improvement
### Individual Tests

Function1 name: setup_logging() (in src/borg/logger.py)

Link to commit: https://github.com/AlexandruMititelu/A1.1-SEP-RESIT/commit/b1e85b473ddd7a0569d2cf721af43170ba145037

Screenshot of before :<br/> 
![alt text](image-2.png)
Screenshot of after:<br/> 
![alt text](image-2.png)

Function2 name: do_help() (in src/borg/archiver/help_cmd.py)

Link to commit: https://github.com/AlexandruMititelu/A1.1-SEP-RESIT/commit/b1e85b473ddd7a0569d2cf721af43170ba145037

Screenshot of before :<br/> 
![alt text](image-2.png)
Screenshot of after:<br/> 
![alt text](image-2.png)


As is easily visible from the screenshots, the coverage in that particular file was improved from 78% to 82%. This can be attributed to the fact that a specific test that is meant to trigger the 'branch 2' of the function was added to the already existing tests in the testsuite. This 'test_setup_logging_with_config_file()' test is testing the setting up of a logger when a config file is provided to the function and this is a conditional branch that was not tested before. To test this a temporary config file was written and provided to the setup function (another function had to be adapted slightly as well). Furthermore in the screenshot one can see that this 'branch 2' is now being reached thanks to the additional test and even the already existent coverage measurement tool reports an increase in coverage in that specific file.

### Overall

Screenshot of result, overall coverage:<br/>
![alt text](Photos/OG_coverage.png)
Screenshot of result, overall coverage of the file we are going to modify:<br/>
![alt text](Photos/OG_coverage2.png)


Tool coverage measurement (old):<br/>
![alt text](image-10.png)

Tool coverage measurement (new):<br/>
![alt text](image-11.png)

As is seen in the screenshots, the coverage in that particular file was improved from 85% to 100%. If one checks the lines that were missing before and compares it to the old code (before the manual branch logging was added) one can easily see that the missing lines correspond to one specific else branch. This can also be seen in the manual logging that all code except this one else statement (in the file but also every branch in this specific function) is reached by the tests. This else-statement corresponds to there not being helpful documentation for the topic the person is invoking the help command for. The tests show an easy improvement being made by trying to invoke the help command with a topic that is not in the documentation in the same manner the already existing tests did. This enhanced the coverage as now every branch of every function in that file is being hit with the test cases.

### Overall

Old coverage result:<br/>
![alt text](image-1.png)

Link to the slides:
https://docs.google.com/presentation/d/1FqbQYH7BRJwMV4EC2VnmxTNJajOnKH8YlXyUeRCZzvY/edit?usp=drive_link
