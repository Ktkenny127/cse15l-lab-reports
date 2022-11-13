## Using Vim

# Changing Start to Base

To change thevariable start to base in DocSearchServer.java, I fist opened the file using vim with:

``` vim DocSearchServer.java ```

This opened the file to look like this

![Alt text](Open%20Vim.png)

Then I beagn by searching for the word start using ``` /start <Enter> ``` shown below

![Alt text](search.png)

Once I was on the first instance of start I used ``` ce base <Escape> ``` which entered insert mode ` e ` deleted the word then I changed to base then exited insert mode

![Alt text](Start%20to%20base.png)

After changing the first start and exited insert mode I then pressed ``` n. ``` to go to the next instance of start and do the same edit to this start.

![Alt text](N%20to%20dot.png)

I then did the same process f ``` n. ``` to do edit the last instance of start that hasd to be inserted.

![Alt text](Again.png)

To exit I used ``` :wq ``` to save and exit and save vim.
