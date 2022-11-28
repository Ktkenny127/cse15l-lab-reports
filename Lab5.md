# Grading Script
## Grade.sh Code
``` CPATH=".:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar"
 f="student-submission/ListExamples.java"


 rm -rf student-submission
 git clone $1 student-submission
 cp TestListExamples.java student-submission/

 if [[ -f $f ]] && [[ -e $f ]]
 then
    echo "File exists!"
 else
    echo "File not found!"
    exit 1
 fi

  cd student-submission

 java -cp $CPATH  org.junit.runner.JUnitCore TestListExamples > failures.txt 

 if [[ $(grep -c "testFilter(TestListExamples)" failures.txt) -ne 0 ]]
 then
    echo "FAILED testFilter"
 else
    echo "PASSED testFilter"
 fi

 if [[ $(grep -c "testMerge(TestListExamples)" failures.txt) -ne 0 ]]
 then
    echo "FAILED testMerge"
 else
    echo "PASSED testMerge"
 fi
```
This is my grade.sh script that is used to test ListExamples.java.

## Graded Repos
![](One%20Test.png)

This is the fixed version of the code from Lab3. This code first goes through the
 ```
 rm -rf student-submission
 git clone $1 student-submission
 cp TestListExamples.java student-submission/
 ```
 
Once it goes througha dn gets rid of the directory and clones the new one, and copies tyhe graders TestListExamples over to the students directory it then goes to the if statement where it is making sure there is a file in the name of ListExamples and since there it is echos that tghe file exists then skips then else and endss the if. Then the codes goes into the student submission, and runs the TestExamples and puts it into the failures.txt file. Once everythig is in the filew it then goes and checks to see if there are any mathed lines to "testFilter(TestListExamples)" and since there arent it outputs that the test passed and skips the other else statement. This happens again for the other test. 

Here is another example of the code runniong through a repository

![](Good%20in%20diff%20directory.png)

And just one more:

![](File%20Not%20Found.png)

That is all that my grader has to entail!