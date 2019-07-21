## Supported server types:
1. Windows 32Bit, 64Bit, Linux 32Bit
# Exile 64bit Edition Conversion
1. Open your @ExileServer Folder and delete the following files : extDB2.dll , extDB2.so , extDB2-conf.ini , XM8.dll , XM8.so
2. Download the git release of the Exdb3 Exile patch (https://github.com/BrettNordin/Exile) Press the clone/download button.
3. Copy the @ExileServer file into the server directory
4. Copy the contents of Exile.MapName INTO your mission file.
5. Open your config.cpp and do the following:

In your config.cpp 
Add: #include "CfgExileCustomCode.cpp" 
Into:
class CfgExileCustomCode 
{
};

It will look like this in the end: 

    class CfgExileCustomCode 
    {
        #include "CfgExileCustomCode.cpp" 
    };



6. Copy the TWO tbbmalloc.dll's (tbbmalloc.dll, tbbmalloc_x64.dll) to your server ROOT directory
### Only do #10 if you are not a freshly installed exile server. 
7. Exit the Exile.ini file to match any changes in your older exile.ini
 SIDENOTE: the new exile.ini no longer contains the lines with "Number of Inputs = #" (# is referring to any number within the file on this line)
8. Run the Mysql Querys in the "Exile_Database_Update_64x.sql" file to properly update your database.


## Go to https://github.com/BrettNordin/Exile/wiki/Common-Errors--&-Issues for help with most issues.
