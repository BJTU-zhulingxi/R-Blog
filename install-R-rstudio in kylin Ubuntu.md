# install R in Kylin Ubuntu

Fist I try to install R  with the apt-get command,but I don't know if it can worked or not.but just try it.

Becasue the have just installed the new Kylin Ubuntu system,so I'd like to try with the easyest way to set up R in Ubuntu.

Just use the command 

    $sudo apt-get install r-base r-base-dev
		
After the command has finished,I checked it.

    $R

The R runed without any problem,then I checked the version of R.

    >version
    platform       x86_64-pc-linux-gnu         
    arch           x86_64                      
    os             linux-gnu                   
    system         x86_64, linux-gnu           
    status                                     
    major          3                           
    minor          2.3                         
    year           2015                        
    month          12                          
    day            10                          
    svn rev        69752                       
    language       R                           
    version.string R version 3.2.3 (2015-12-10)
    nickname       Wooden Christmas-Tree       

 The version is 3.2.3,it is the latest version of R.So it worked well by the apt-get command.
 
You can reference this two blog when you need to install R in your Ubuntu,I think this two will enough for you to deal with this task at normal situation.
 

["install R and RSstudio in Ubuntu"](http://) http://blog.csdn.net/lichangzai/article/details/39376117
 
["Install R in Ubuntu"](http://)http://sites.psu.edu/theubunturblog/installing-r-in-ubuntu/
 

# install r-studio in ubuntu
 
 first I try to install R-Studio Server iin Ubuntu.
 
 I read the guide of the R-studio web sit,and followed the process.

[**install rstudio-server**](https://www.rstudio.com/products/rstudio/download-server/)
 
First you install the gdebi-core.
 
    $sudo apt-get install gdebi-core

Then you should install rstudio-server from the command line.If your PC is 32bit you should install the i386 version of rstudio-server,follow the steps below:

    $wget https://download2.rstudio.org/rstudio-server-1.0.44-i386.deb
    $sudo gdebi rstudio-server-1.0.44-i386.deb

But if your PC is 64bit,you should install the 64bit version,like showned below:

    $ wget https://download2.rstudio.org/rstudio-server-1.0.44-amd64.deb
    $ sudo gdebi rstudio-server-1.0.44-amd64.deb

After the installation finished,you can start r-studio by type :

    $sudo rstudio-server restart
		
if you want to use rstudio-server,you can only use it in Browser.

you type the url in your browser.

	http://192.168.1.102:8787/

use the use as your linux usr and the password.

but if you restart the system,rstudio-server will not start automaticly,so you must start it manully

The rstudio-server utility is installed under /usr/sbin.So you must enter the directory and start it.
