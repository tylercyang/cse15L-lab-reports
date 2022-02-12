# Lab Report 3 - Streamlining ssh Configuration

>As of right now, logging using `ssh` to log into a specific remote account is slightly annoying, even with the improvement that we made using a ssh key. Currently, logging into ieng6 for example should look something like this...

![current ssh](Lab-Report-3-Photos\first.png)

>Typing out your specific account information is long and tedious so we can improve that by creating a configuration file to streamline this process. 

>There should already be a `.ssh\` folder on your computer from the last time we created a ssh key. Open that folder and create a new filed called `config`. Now, copy this into your folder...

![config file](Lab-Report-3-Photos\second.png)

>Changing the `apb` to your specific ieng6 account. Then run the command `ssh ieng6` in your terminal and it should log you into ieng6 immediately. 

![login](Lab-Report-3-Photos\third.png)

>If this does not work for you, try adding an extra line at the bottom to specify the file that you are running...

![extra line](Lab-Report-3-Photos\fourth.png)

>Additionally, you can change the host name `ieng6` to another name that you want and it should still work. Now that you are easily able to log into ieng6, you can also more easily `scp` files and repositories into ieng6 as well. This could look something like this...

![](Lab-Report-3-Photos\fifth.png)