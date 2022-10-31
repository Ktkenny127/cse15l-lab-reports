# Reasearching Commands

## Find

The first command I tholught was interesting was the type command where it finds different type of files sucha as directories like the example below

    $ find . -type d
    
    .
    ./911report
    ./biomed
    ./government
    ./government/About_LSC
    ./government/Alcohol_Problems
    ./government/Env_Prot_Agen
    ./government/Gen_Account_Office
    ./government/Media
    ./government/Post_Rate_Comm
    ./plos
This command uses the indicator of -d to tell that you want to search for directories. SO it will print out all the directories in the file you are looking for. 


There are oither types of typoes aswell the type f is just a normal file. It is shown below.
    find . -type f
    ./plos/pmed.0020235.txt
    ./plos/pmed.0020236.txt
    ./plos/pmed.0020237.txt
    ./plos/pmed.0020238.txt
    ./plos/pmed.0020239.txt
    ./plos/pmed.0020242.txt
    ./plos/pmed.0020246.txt
    ./plos/pmed.0020247.txt
    ./plos/pmed.0020249.txt
    ./plos/pmed.0020257.txt
    ./plos/pmed.0020258.txt
    ./plos/pmed.0020268.txt
    ./plos/pmed.0020272.txt
    ./plos/pmed.0020273.txt
    ./plos/pmed.0020274.txt
    ./plos/pmed.0020275.txt
    ./plos/pmed.0020278.txt
    ./plos/pmed.0020281.txt
    
The abvove code is just a snippet of what type f's output since it outpusts every normal file and there are around 1400 file in technical. 

The next typoe has no output becasue there is nothign tov output.
    find . -type d -empty
    find . -type l

These two commands are interesting to me. The first one find all the empty directories which as of right nowe in technical there are none so thats why tyhe output is nothing but it is interesting none the less. The other command is meant to find all of the 'file links' which I dont know what they are but it had no output which is iunteresting.
