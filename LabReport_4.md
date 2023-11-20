### Steps (4-9) Screenshots & Commands 
##### - Logged into ieng account : ssh dreyesgomez@ieng6.ucsd.edu + `<enter>`
![image](https://github.com/dreyes32/cse15l-lab-reports/assets/146775725/5513b406-0e63-48d2-8580-aae63976aa9a)

##### - Used command: `rm -rf lab7` to delete past directory of it, then I did command : `git clone git@github.com:dreyes32/lab7.git` + `<enter>`
![image](https://github.com/dreyes32/cse15l-lab-reports/assets/146775725/1fd6077d-1ac9-4433-b712-a964e0da59d8)


##### - I cd into lab7, then ran both these commands to compile and run (Showing errors): `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` + `<enter>` & `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` + `<enter>`
![image](https://github.com/dreyes32/cse15l-lab-reports/assets/146775725/5ee87484-aa92-468f-aa08-f19184293b4b)


##### - Ran command: `vim ListExamples.java` `<enter>`, then fixed error by going to the line of error: `<Right>` * 11 + x (deleting the 1 from the index) + i (insert mode) typed "2" to replace and fix + `<esc>` + :wq (Save and Exit)
![image](https://github.com/dreyes32/cse15l-lab-reports/assets/146775725/a1950737-002e-41c7-9772-86d1e32de358)

##### - Now we must recompile and run : `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` + `<enter>` & `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` `<enter>` 
![image](https://github.com/dreyes32/cse15l-lab-reports/assets/146775725/c320bb4a-d9cb-4961-ad1b-a5fa89ab859a)

##### - Now we must do command: `git add ListExamples.java`(stages for commit, basically sends it so it can be committed) + `<enter>` , git commit -m "some message" (actually saves the changes) + `<enter>`, git push + `<enter>` (uploads local repo to remote)
![image](https://github.com/dreyes32/cse15l-lab-reports/assets/146775725/992b357b-f718-4a8a-9e4d-a1949ab5fac2)






