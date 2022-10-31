# Reasearching Commands

## Find -type

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

These two commands are interesting to me. The first one find all the empty directories which as of right nowe in technical there are none so thats why tyhe output is nothing but it is interesting none the less. The other command is meant to find all of the 'file links' which I dont know what they are but it had no output which is interesting.


## Find -perm

Another interesesting commands line option I found for find was -perm. It searches for files wioth certain permissions which I think is intersesting.\

    find . -perm /222

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

The output is much loinger than this sisnce I just searcheds gfor files that are writable by someone which is not specific enough top bring up only a few files.

    find . -perm -664

Spewaking of a few files this command this commands search for files which have read and write permission for their owner and group, and which other users can read, without regard to the presence of any extra permission bits. And appareently none of those exist in this directory

    find . -perm -220

This also outpouts nothing but it seaarches for files which are writable by both their owner and their group which there are none.

## Find -daystart

The last commands that IU found interesting was anything to do with the daystart option.

    $ find . -mtime -12

    ./plos/journal.pbio.0020267.txt
    ./plos/journal.pbio.0020272.txt
    ./plos/journal.pbio.0020276.txt
    ./plos/journal.pbio.0020297.txt
    ./plos/journal.pbio.0020302.txt
    ./plos/journal.pbio.0020306.txt
    ./plos/journal.pbio.0020307.txt
    ./plos/journal.pbio.0020310.txt
    ./plos/journal.pbio.0020311.txt
    ./plos/journal.pbio.0020337.txt
    ./plos/journal.pbio.0020346.txt
    ./plos/journal.pbio.0020347.txt
    ./plos/journal.pbio.0020348.txt
    ./plos/journal.pbio.0020350.txt
    ./plos/journal.pbio.0020353.txt
    ./plos/journal.pbio.0020354.txt
    ./plos/journal.pbio.0020394.txt
    ./plos/journal.pbio.0020400.txt
    ./plos/journal.pbio.0020401.txt
    ./plos/journal.pbio.0020404.txt
    ./plos/journal.pbio.0020406.txt
    ./plos/journal.pbio.0020419.txt
    ./plos/journal.pbio.0020420.txt
    ./plos/journal.pbio.0020430.txt
    ./plos/journal.pbio.0020431.txt
    ./plos/journal.pbio.0020439.txt

This command the mtime option gives you the time of when something wsas made or last edited. It uses how many days as the parameter and since I forked the repository it is all abnout 12-13 dasys old so all files show up when I typed the command above

    find . -mmin -15

    ./911report/chapter1.txt

I went in an  edited a file by deletring a new line and then used the mmin which takes minutes instead of dasy as the parameter and since the only other file to be edited in 13 dasy ago was the one i did less than 15 minutes ago it prints that file.

    $ find . -ctime -12

    ./plos/journal.pbio.0020267.txt
    ./plos/journal.pbio.0020272.txt
    ./plos/journal.pbio.0020276.txt
    ./plos/journal.pbio.0020297.txt
    ./plos/journal.pbio.0020302.txt
    ./plos/journal.pbio.0020306.txt
    ./plos/journal.pbio.0020307.txt
    ./plos/journal.pbio.0020310.txt
    ./plos/journal.pbio.0020311.txt
    ./plos/journal.pbio.0020337.txt
    ./plos/journal.pbio.0020346.txt
    ./plos/journal.pbio.0020347.txt
    ./plos/journal.pbio.0020348.txt
    ./plos/journal.pbio.0020350.txt
    ./plos/journal.pbio.0020353.txt
    ./plos/journal.pbio.0020354.txt
    ./plos/journal.pbio.0020394.txt
    ./plos/journal.pbio.0020400.txt
    ./plos/journal.pbio.0020401.txt
    ./plos/journal.pbio.0020404.txt
    ./plos/journal.pbio.0020406.txt
    ./plos/journal.pbio.0020419.txt
    ./plos/journal.pbio.0020420.txt
    ./plos/journal.pbio.0020430.txt
    ./plos/journal.pbio.0020431.txt
    ./plos/journal.pbio.0020439.txt

The command above essentially does the exact same thing as the first command but it uses a different option wiuthing the daystream catagory. The + or - can mean above or below the certtain trime range you inster respectivly.